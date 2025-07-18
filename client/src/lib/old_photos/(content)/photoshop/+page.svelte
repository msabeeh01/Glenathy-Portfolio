<script>
	import MasonryItem from '$lib/Masonry/MasonryItem.svelte';

	// get images from photoshop_images folder
	import typography from '$lib/digital_images/photoshop_images/Chan-Choong_Glen_S4_Exercise6.jpg';
	import magazine_cover from '$lib/digital_images/photoshop_images/Chan-Choong_Glen_Section4_LTL.jpg';
	import album_cover from '$lib/digital_images/photoshop_images/Chan-Choong_Glen_Section4_CDCover.jpg';

	import { onMount } from 'svelte';
	import AOS from 'aos';

	onMount(() => {
		AOS.init();
	})
</script>

<div class="flex flex-col h-full w-full place-items-center">
	<div class="my-auto items-center flex flex-col gap-4">
		<h1 class="text-3xl font-bold text-[#F7D5B1]">Photoshop Projects</h1>
		<div class="py-5 grid grid-cols-1 md:grid-cols-3 gap-4" data-aos="fade-up">
			<!-- image with description when hovered -->
			<!-- MasonryItem 5 times -->
			<MasonryItem title="Text Effect Project: Spray Paint Effect" img={typography} />
			<MasonryItem
				title="Magazine Cover Project: Cyberpunk Fashion Magazine"
				img={magazine_cover}
			/>
			<MasonryItem
				title="Album Cover Project: Single Cover Art for Hojean's Single, Memory"
				img={album_cover}
			/>
		</div>
	</div>
</div>
