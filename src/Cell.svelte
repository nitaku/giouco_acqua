<script>
	export let cell
	export let cellsize

	function handleClick() {
		cell.direction += 45
	}
</script>

<g on:click={handleClick}>
	<rect width={cellsize} height={cellsize}/>
	<path d="M-15 -7 L0 0 L-15 7 Z" transform="translate({cellsize/2} {cellsize/2}) rotate({cell.direction}) translate({cellsize/2} 0)"/>
</g>

<style>
	rect {
		fill: white;
		stroke: steelblue;
		stroke-width: 2;
	}
	path {
		fill: steelblue;
	}
</style>