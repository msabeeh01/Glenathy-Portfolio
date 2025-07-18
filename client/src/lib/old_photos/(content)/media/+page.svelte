<script>
	//import the ImageCard component
	import ImageCardLinked from "$lib/ImageCard/ImageCardLinked.svelte";
    import { onMount } from 'svelte';
    import AOS from 'aos';

    import parking from '$lib/digital_images/film_images/parking.png';
    import glensky from '$lib/digital_images/digital_images/glensky.png';

    onMount(() => {
        AOS.init();
    })
</script>

<div data-aos="fade-up" class="flex flex-col place-items-center gap-4 text-center md:flex-row h-full w-full">
		<ImageCardLinked title="Digital" year="2023" image={glensky} href="/digital"/>
		<ImageCardLinked title="Film" year="2023" image={parking} href="/film" />

</div>


