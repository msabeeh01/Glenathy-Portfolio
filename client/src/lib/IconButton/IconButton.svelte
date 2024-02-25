<script>
	/**
	 * @type {string}
	 */
	export let link
</script>

<div>
	<a href={link}>
	<button class="hover:scale-105 transition duration-300 hover:bg-[#FBFFE0] hover:text-black hover:shadow-sm">
		<slot />
	</button>
</a>
</div>

<style>
	button {
		border-radius: 100px;
		color: #F7D5B1;
		background-color: #2C3950;
		line-height: 40px;
		margin: 0 auto;
		font-weight: bold;
		border: none;
		height: 30px;
		width: 30px;
		padding: 4px
	}
</style>
