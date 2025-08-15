<script lang="ts">
	import { onMount } from 'svelte';
	import '../app.css';
	import { imgArray } from '../constants/data';
	import { ScrollTrigger } from 'gsap/all';
	import gsap from 'gsap';
	import Typography from '../components/Typography/typography.svelte';
	import ProjectGridItem from '../components/Typography/ProjectGrid/ProjectGridItem.svelte';
	let name = 'Glen Chan-Choong';

	if (typeof window !== 'undefined') {
		gsap.registerPlugin(ScrollTrigger);
	}

	//array of images and their description
	let ctx: gsap.Context;

	onMount(() => {
		ctx = gsap.context(() => {
			gsap.fromTo(
				'.name',
				{
					yPercent: 100,
					opacity: 0
				},
				{
					yPercent: 0,
					opacity: 1,
					duration: 0.5
				}
			);

			gsap.fromTo(
				'.projectitem',
				{
					yPercent: 100,
					opacity: 0
				},
				{
					yPercent: 0,
					opacity: 1,
					duration: 0.5,
					stagger: 0.1,
					ease: 'power2.out',
					delay: 0.2
				}
			);
		});
	
		return () => {
			ctx.revert();
		};
	});
</script>

<!-- children should be same width -->
<div class="w-screen bg-white mb-[300px]">
	<!-- Main Container, seperate from page container -->
	<div class="flex flex-col gap-[76px] py-[70px] mx-auto max-w-[1200px] h-full px-[70px] z-10">
		<!-- NAVBAR -->
		<div class="flex justify-between text-[#3589FF] items-center overflow-hidden pb-2">
			<div class="name">
				<Typography type="heading" as="h1">{name}</Typography>
			</div>
			<!-- <ul class="list-none flex flex-row gap-[40px]">
				<a href="#">ITEM 1</a>
				<a href="#">ITEM 2</a>
				<a href="#">ITEM 3</a>
			</ul> -->
		</div>

		<!-- SHORT INFO SECTION -->
		<div class="w-full lg:w-[55%] h-fit overflow-hidden">
			<Typography type="paragraph" class="name" as="p">
				Hi, I’m {name}— a Toronto-based Graphic Designer with a passion for storytelling and a sharp
				eye for detail. I’ve crafted visual identities, led creative projects, and brought ideas to
				life through bold, effective design.
			</Typography>
		</div>

		<!-- 3X4 grid (400px X 400px) -->
		<div class="flex flex-col md:grid md:grid-cols-2 lg:grid-cols-3 w-full overflow-hidden">
			{#each imgArray as item, index}
				<div class="projectitem">
					<ProjectGridItem {item} />
				</div>
			{/each}
		</div>
	</div>

	<div class="text-white p-4 bg-[#3589FF] fixed bottom-0 w-full flex items-end h-[300px] -z-10">
		<h2>Contact Info</h2>
	</div>
</div>
