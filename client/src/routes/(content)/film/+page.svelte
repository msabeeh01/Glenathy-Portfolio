<script>
	import MasonryItem from '$lib/Masonry/MasonryItem.svelte';

	import bar from '$lib/digital_images/film_images/bar.png';
	import crowd from '$lib/digital_images/film_images/crowd.png';
	import parking from '$lib/digital_images/film_images/parking.png';
	import singer from '$lib/digital_images/film_images/singer.png';
	import roof from '$lib/digital_images/film_images/roof.jpg';
	import fountain from '$lib/digital_images/film_images/fountain.jpg';

	import { onMount } from 'svelte';
	import AOS from 'aos';

	onMount(() => {
		AOS.init();
	})
</script>

<div class="h-full w-full">
	<!-- image with description when hovered -->
	<div class="my-auto items-center flex flex-col gap-4" data-aos="fade-up">
		<div class="flex justify-center items-center">
			<h1 class="text-3xl font-bold text-[#F7D5B1]">Film</h1>
		</div>

		<!-- MasonryItem 5 times -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-4 w-full">
			<MasonryItem title="" img={singer} />
			<MasonryItem title="" img={parking} />

			<div class="md:col-span-2 w-full">
				<MasonryItem title="" img={bar} />
			</div>

			<MasonryItem title="" img={crowd} />
			<MasonryItem title="" img={roof} />

			<div class="md:col-span-2 w-full">
				<MasonryItem title="" img={fountain} />
			</div>
		</div>
	</div>
</div>
