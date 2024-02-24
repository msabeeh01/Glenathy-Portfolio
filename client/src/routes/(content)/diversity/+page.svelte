<script>
	import MasonryItem from '$lib/Masonry/MasonryItem.svelte';

	// get images from photoshop_images folder
    import exec_jack from '$lib/digital_images/diversity_images/exec takeover post- main - Jack-01.png';
    import exec_main from '$lib/digital_images/diversity_images/exec takeover post- main-01.png';

    import exec_post from '$lib/digital_images/diversity_images/exec takeover post - Jack-01.png';
    import story_post from '$lib/digital_images/diversity_images/exec takeover story post.png';
</script>

<div class="flex flex-col place-items-center h-full w-full">
    <div class="flex place-items-center text-center text-[#F7D5B1]">
    <h1 class="text-3xl font-bold text-[#F7D5B1]">Representing Diversity in Law</h1>
</div>
	<div class="py-5 grid grid-cols-1 md:grid-cols-3 gap-4">
		<MasonryItem title="Text Effect Project: Spray Paint Effect" img={exec_jack} />
		<MasonryItem title="Magazine Cover Project: Cyberpunk Fashion Magazine" img={exec_main} />
		<MasonryItem
			title="Album Cover Project: Single Cover Art for Hojean's Single, Memory"
			img={exec_post}
		/>
        <MasonryItem
			title="As"
			img={story_post}
		/>
	</div>
</div>
