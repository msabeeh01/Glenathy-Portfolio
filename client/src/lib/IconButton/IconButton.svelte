<script>
	/**
	 * @type {string}
	 */
	export let link
</script>

<div>
	<a href={link}>
	<button>
		<slot />
	</button>
</a>
</div>

<style>
	button {
		border-radius: 100px;
		color: black;
		background-color: white;
		line-height: 40px;
		margin: 0 auto;
		font-weight: bold;
		border: none;
		height: 30px;
		width: 30px;
	}
</style>
