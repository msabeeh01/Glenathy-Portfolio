<script>
	//import the ImageCard component
	import ImageCard from '$lib/ImageCard/ImageCard.svelte';
</script>

<div
	class="flex flex-col place-items-center gap-10 sm:py-10 lg:py-0 text-center md:grid md:grid-cols-2 lg:grid-cols-3 w-[80%] h-full"
>
	<a href="/photoshop">
		<ImageCard
			image="https://cdn.myportfolio.com/7bf13fc8-be3c-4bd4-96b0-ae0f57e2689c/6bf73db8-7b11-419f-957a-f63059908643_carw_202x158x640.jpg?h=5c5fe546c0af429ca9869d8284d761ec"
			title="Photoshop Projects"
			year="2023"
		/>
	</a>

	<a href="/diversity">
		<ImageCard
			image="https://cdn.myportfolio.com/7bf13fc8-be3c-4bd4-96b0-ae0f57e2689c/4bed043d-70a3-4cfc-a09a-d05480a2e5d0_rwc_0x492x4510x3526x640.png?h=bfcdd71fd6a5e2531ad27dff1eba7ec9"
			title="Representing Diversity in Law"
			year="2022"
		/>
	</a>

	<a href="/illustrator">
	<ImageCard
		image="https://cdn.myportfolio.com/7bf13fc8-be3c-4bd4-96b0-ae0f57e2689c/ae26f53b-04f8-46e4-98b4-cf4c83690a98_rwc_0x499x4576x3577x640.jpg?h=069edce2950937b768394dec7455fcef"
		title="Illustrator Projects"
		year="2021"
	/>
	</a>
</div>
