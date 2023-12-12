<script>
	export let text = 'Button';
    export let link = '/';
</script>

<a href={link}>
	<button class="hover:scale-105 transition duration-300 hover:bg-[#FBFFE0] hover:text-black hover:shadow-sm">
		{text}
	</button>
</a>

<style>
	button {
		border-radius: 100px;
		color: white;
		background-color: #222222;
		line-height: 40px;
		margin: 0 auto;
		padding: 0 30px;
		font-weight: bold;
		border: none;
	}
</style>
