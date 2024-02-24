<script>
    /** @type {import('./$types').PageData} */
    export let data;
    import MasonryItem from "$lib/Masonry/MasonryItem.svelte";

    import stoicism from '$lib/digital_images/illustrator_images/GCM 320 Proj4 - Chan-Choong Glen-01.png';

    import akutagawa from '$lib/digital_images/illustrator_images/Akutagawa_Ryuunosuke.png';
    import hakka from '$lib/digital_images/illustrator_images/Hakka Designs Main-01.jpg';
    import levi from '$lib/digital_images/illustrator_images/Levi-01.png';
    import nobara from '$lib/digital_images/illustrator_images/Nobara-01.png';
</script>

<div class="flex flex-col place-items-center h-full w-full">

    <div class="flex place-items-center text-center text-[#F7D5B1]">
        <h1 class="text-3xl font-bold pb-8">Illustrator Projects</h1>
    </div>

    <!-- main image -->
    <div class="md:h-5/6">
        <img src="{stoicism}" class="object-contain h-full w-full rounded-md" alt="Digital" />
    </div>

    <!-- grid -->
    <div class="py-5 grid grid-cols-1 md:grid-cols-3 gap-4">
        <MasonryItem title="Image" img="{akutagawa}"/>
        <MasonryItem title="Image" img="{hakka}"/>
        <MasonryItem title="Image" img="{levi}"/>
        <MasonryItem title="Image" img="{nobara}"/>

    </div>
</div>