<script>
	import MasonryItem from '$lib/Masonry/MasonryItem.svelte';

	import glensky from '$lib/digital_images/digital_images/glensky.png';
	import sunsetphoto from '$lib/digital_images/digital_images/sunsetphoto.png';
	import twoguys from '$lib/digital_images/digital_images/twoguys.png';
</script>

<div class="h-full w-full flex flex-col place-items-center">
	<!-- image with description when hovered -->
	<!-- MasonryItem 5 times -->
	<div class="my-auto items-center flex flex-col gap-4">
		<div class="flex place-items-center text-center text-[#F7D5B1]">
			<h1 class="text-3xl font-bold text-[#F7D5B1]">Digital</h1>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 items-center">
			<MasonryItem title="" img={glensky} />
			<MasonryItem title="" img={twoguys} />
			<MasonryItem title="" img={sunsetphoto} />
		</div>
	</div>
</div>
