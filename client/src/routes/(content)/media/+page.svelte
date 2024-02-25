<script>
	//import the ImageCard component
	import ImageCardLinked from "$lib/ImageCard/ImageCardLinked.svelte";
    import { onMount } from 'svelte';
    import AOS from 'aos';

    import parking from '$lib/digital_images/film_images/parking.png';

    onMount(() => {
        AOS.init();
    })
</script>

<div data-aos="fade-up" class="flex flex-col place-items-center gap-4 text-center md:flex-row h-full w-full">
		<ImageCardLinked title="Digital" year="2023" image="https://cdn.myportfolio.com/7bf13fc8-be3c-4bd4-96b0-ae0f57e2689c/f29c8721-35bb-49c5-aee4-e2958be0cce3.png?h=5ab12f7f86bce98f81301e35b4a4acc7" href="/digital"/>
		<ImageCardLinked title="Film" year="2023" image={parking} href="/film" />

</div>


