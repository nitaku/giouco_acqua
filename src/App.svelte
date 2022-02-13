<script>
	import * as d3 from 'd3'

	import Board from './Board.svelte'

	const rows = 6
	const cols = 6
	const cellsize = 60
	const padding = 10

	let matrix = d3.range(rows).map( (row) => d3.range(cols).map( (col) => ({row, col, direction: 45}) ))
	$: cells = matrix.flat()
</script>

<svg width={(cellsize+padding)*cols+padding} height={(cellsize+padding)*rows+padding}>
	<g transform="translate({padding} {padding})">
		<Board {cells} {cellsize} {padding}/>
	</g>
</svg>

<style>
</style>