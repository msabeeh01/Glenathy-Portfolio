<script>
// @ts-nocheck

	//props
	// @ts-ignore
	export let title;
	// @ts-ignore
	export let year;
	// @ts-ignore
	export let image;
	// @ts-ignore
	export let href;
</script>

<div
	class="item hover:scale-105 transition bg-[#2C3950] duration-300 text-[#F7D5B1] hover:text-black hover:bg-[#F7D5B1] shadow-xl hover:shadow-lg font-bold rounded-xl"
>
	<a {href} class="w-full">
		<img src={image} alt="alt" class="rounded-t object-cover" />
		<div class="text">
			<p>{title}</p>
			<p class="text-sm">{year}</p>
		</div>
	</a>
</div>

<style>
	.item {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		width: 100%;
	}

	img {
		width: 100%;
		height: 400px;
	}

	.text {
		font-size: 24px;
		padding: 2rem;
	}
</style>
