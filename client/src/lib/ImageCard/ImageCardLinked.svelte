<script>
    //props
    export let title
    export let year
    export let image
    export let href
</script>

<div class="item hover:scale-105 transition duration-300 hover:bg-[#FBFFE0] hover:shadow-sm font-bold rounded-md">
    <a href={href}>
    <img src={image} alt="image alt" class="rounded-t"/>
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