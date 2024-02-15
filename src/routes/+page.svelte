<script>
	import Board from '../Board.svelte';
</script>

<div class="screen">
	<div class="board-area">
		<Board />
	</div>
	<div class="eval-area"></div>
	<div class="move-area"></div>
</div>

<style>
	.screen {
		display: grid;
		inset: 1fr;
		width: 100%;
		height: 100%;

		grid-template-areas:
			'b b b e e'
			'b b b e e'
			'b b b e e'
			'b b b e e'
			'm m m m m';
		grid-template-columns: 3fr 2fr;
		grid-template-rows: 4fr 1fr;
	}
	.board-area {
		grid-area: 'b';
	}
	.eval-area {
		grid-area: 'e';
	}
	.move-area {
		grid-area: 'm';
	}
</style>
