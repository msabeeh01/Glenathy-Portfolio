<script>
	//import the ImageCard component
	import ImageCard from '$lib/ImageCard/ImageCard.svelte';
	import { onMount } from 'svelte';
	import AOS from 'aos';

	import cdcover from '$lib/digital_images/photoshop_images/Chan-Choong_Glen_Section4_CDCover.jpg';
	import jack from '$lib/digital_images/diversity_images/exec takeover post- main - Jack-01.webp';
	import hakka from '$lib/digital_images/illustrator_images/Hakka Designs Main-01.jpg';

	onMount(() => {
		AOS.init();
	});
</script>

<div
	data-aos="fade-up"
	class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 place-items-center gap-4 text-center w-full h-full"
>
	<a href="/photoshop">
		<ImageCard
			image={cdcover}
			title="Photoshop Projects"
			year="2023"
		/>
	</a>

	<a href="/diversity">
		<ImageCard
			image={jack}
			title="Representing Diversity in Law"
			year="2022"
		/>
	</a>

	<a href="/illustrator">
		<ImageCard
			image={hakka}
			title="Illustrator Projects"
			year="2021"
		/>
	</a>
</div>
