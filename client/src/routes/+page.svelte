<script lang="ts">
	import { onMount } from 'svelte';
	import '../app.css';
	import { imgArray } from '../constants/data';

	import ProjectGridItem from '../components/Typography/ProjectGrid/ProjectGridItem.svelte';

	import {gsap} from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';
	import { ScrollSmoother } from 'gsap/ScrollSmoother.js';
	import Hero from '../components/home/Hero/Hero.svelte';
	import Footer from '../components/navigation/Footer.svelte';

	if (typeof window !== 'undefined') {
		gsap.registerPlugin(ScrollTrigger, ScrollSmoother);
	}

	//array of images and their description
	let ctx : gsap.Context;
	let smoother: ScrollSmoother 

	onMount(() => {
		// Add snap functionality
		let snapSections = gsap.utils.toArray('.snap-section');
		smoother = ScrollSmoother.create({
		smooth: 1,
		effects: true,

		wrapper: '.smooth-wrapper',
		content: '.smooth-content'
	});

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
					duration: 1
				}
			);

			gsap.set('.projectitem', {
				yPercent: 100,
				opacity: 0
			});

			// Animate each item individually
			gsap.to('.projectitem', {
				yPercent: 0,
				opacity: 1,
				duration: 0.8,
				stagger: 0.1,
				scrollTrigger: {
					trigger: '.projectAnimationTrigger',
					start: 'top center',
					end: 'bottom center',
					markers: true,
					toggleActions: 'restart reverse restart reverse'
				}
			});

			snapSections.forEach((section: any, i) => {
				ScrollTrigger.create({
					trigger: section,
					start: 'top center',
					end: 'bottom center',
					onToggle: (self: any) => {
						if (self.isActive) {
							smoother.scrollTo(section, true, 'center center');
						}
					}
				});
			});
		});

		return () => {
			ctx.revert();
		};
	});
</script>

<!-- children should be same width -->
<div class="w-screen bg-white smooth-wrapper">
	<!-- Main Container, seperate from page container -->
	<div class="flex flex-col smooth-content z-10">
		<Hero />

		<div class="w-full bg-white mb-[300px]">
			<div
				class="flex flex-col py-[70px] mx-auto max-w-[1200px] min-h-screen projectAnimationTrigger snap-section"
			>
				<!-- 3X4 grid (400px X 400px) -->
				<div
					class="flex flex-col md:grid md:grid-cols-2 lg:grid-cols-3 w-full h-full overflow-hidden"
				>
					{#each imgArray as item, index}
						<div class="projectitem">
							<ProjectGridItem {item} />
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>

	<Footer />
</div>
