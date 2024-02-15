<script lang="ts">
	const rows = [1, 2, 3, 4, 5, 6, 7, 8];
	const cols = [1, 2, 3, 4, 5, 6, 7, 8];
	function isWhite(row: number, col: number) {
		return (row + col) % 2 == 0;
	}
</script>

<div class="board">
	{#each rows as row}
		{#each cols as col}
			{#if isWhite(row, col)}
				<div class="whiteSquare"></div>
			{:else}
				<div class="blackSquare"></div>
			{/if}
		{/each}
	{/each}
</div>

<style>
	.whiteSquare {
		background-image: url('static/whiteSquare.svg');
	}
	.blackSquare {
		background-image: url('static/blackSquare.svg');
	}
	.board {
		display: grid;
		aspect-ratio: 1 / 1;
		grid-template-columns: repeat(8, 1fr);
		grid-template-rows: repeat(8, 1fr);
	}
</style>
