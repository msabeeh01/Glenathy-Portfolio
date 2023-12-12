<script>
    //props
    export let title
    export let year
    export let image
</script>

<div class="item hover:scale-105 transition duration-300 bg-[#2C3950] shadow-xl hover:text-black text-[#F7D5B1] hover:bg-[#F7D5B1] hover:shadow-sm rounded-md">
    <img src={image} alt="image alt" class="rounded-t"/>
    <div class="text">
        <p class="font-bold">{title}</p>
        <p class="text-sm pt-2">{year}</p>
    </div>
</div>

<style>
    h1 {
        text-align: center;
    }	
    .item {
		display: flex;
		align-items: center;
        justify-content: center;
		flex-direction: column;
		width: 100%;
	}

	.item > img {
		width: 100%;
		height: auto;
	}

	.text {
		font-size: 24px;
		padding: 2rem;
	}
</style>