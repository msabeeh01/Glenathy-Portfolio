<script>
	import MasonryItem from '$lib/Masonry/MasonryItem.svelte';

	import stoicism from '$lib/digital_images/illustrator_images/GCM 320 Proj4 - Chan-Choong Glen-01.png';

	import akutagawa from '$lib/digital_images/illustrator_images/Akutagawa_Ryuunosuke.png';
	import hakka from '$lib/digital_images/illustrator_images/Hakka Designs Main-01.jpg';
	import levi from '$lib/digital_images/illustrator_images/Levi-01.png';
	import nobara from '$lib/digital_images/illustrator_images/Nobara-01.png';

	import { onMount } from 'svelte';
	import AOS from 'aos';

	onMount(() => {
		AOS.init();
	})
</script>

<div class="flex flex-col place-items-center h-full w-full">
	<div class="flex place-items-center text-center text-[#F7D5B1]">
		<h1 class="text-3xl font-bold pb-8">Illustrator Projects</h1>
	</div>

	<div class="flex flex-col h-full w-full" data-aos="fade-up">
		<!-- main image -->
		<div class="md:h-5/6">
			<img src={stoicism} class="object-contain h-full w-full rounded-md" alt="Digital" />
		</div>

		<!-- grid -->
		<div class="py-5 grid grid-cols-1 md:grid-cols-6 gap-4 w-full">
			<div class="col-span-full md:col-span-4 rounded-lg">
				<MasonryItem title="Ryūnosuke Akutagawa artwork from Bungou Stray Dogs" img={akutagawa} />
			</div>

			<div class="col-span-full md:col-span-2">
				<MasonryItem title="Personal Branding" img={hakka} />
			</div>

			<div class="col-span-full md:col-span-3">
				<MasonryItem title="Captain Levi From Attack on Titan Artwork" img={levi} />
			</div>

			<div class="col-span-full md:col-span-3">
				<MasonryItem title="Nobara Artwork from Jujutsu Kaisen" img={nobara} />
			</div>
		</div>
	</div>
</div>
