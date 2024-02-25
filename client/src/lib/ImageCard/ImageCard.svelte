<script>
    // @ts-nocheck
    //props
    export let title;
    export let year;
    export let image;
</script>

<div class="md:h-[500px] item hover:scale-105 transition duration-300 bg-[#2C3950] shadow-xl hover:text-black text-[#F7D5B1] hover:bg-[#F7D5B1] hover:shadow-sm rounded-md">
    <img src={image} alt="alt" class="rounded-t object-cover"/>
    <div class="text text-[24px] p-6 w-full overflow-ellipsis break-words h-full flex flex-col justify-center">
        <p class="font-bold">{title}</p>
        <p class="text-sm pt-2">{year}</p>
    </div>
</div>

<style>
    .item {
		display: flex;
		align-items: center;
		flex-direction: column;
		width: 100%;
	}

</style>