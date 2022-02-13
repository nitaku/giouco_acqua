<script>
	import Cell from './Cell.svelte'

	export let cells
	export let cellsize
	export let padding
</script>

<g>
	{#each cells as cell}
		<g transform="translate({(cellsize+padding)*cell.col} {(cellsize+padding)*cell.row})">
			<Cell {cell} {cellsize}/>
		</g>
	{/each}
</g>

<style>
</style>