<script>
	import { onMount } from 'svelte';
	import AOS from 'aos';

	import glensky from '$lib/digital_images/digital_images/glensky.png';

	onMount(() => {
		AOS.init();
	});
</script>

<div class="flex flex-col h-full w-full">
	<div class="flex justify-center items-center text-[#F7D5B1] pt-5 text-[50px]">
		<h1>About</h1>
	</div>

	<div
		data-aos="fade-up"
		class="shadow-2xl flex bg-[#2C3950] gap-5 md:px-5 md:py-5 rounded-md flex-col lg:flex-row place-items-center text-[#F7D5B1]"
	>
			<img
				class="w-full lg:w-1/2 h-full object-cover rounded-md"
				src={glensky}
				alt="hello"
			/>
		<p class="">
			Hi there! My name is Glen Chan-Choong and I'm a third year Graphic Communications Management
			student at Toronto Metropolitan University (Formerly known as Ryerson University), pursuing a
			minor in Communications and Design. <br /><br />After unearthing my heritage and claiming it
			as my own, I want to be able to not only carry the legacy my ancestors have set out for me,
			but to tell their story and, for myself, help others tell their story through various mediums
			however graphic design and photography are the ones I utilize mainly.
		</p>
	</div>
</div>

<style>
	p {
		font-size: 20px;
		font-family: 'Courier New', Courier, monospace;
		padding: 20px;
	}
</style>
