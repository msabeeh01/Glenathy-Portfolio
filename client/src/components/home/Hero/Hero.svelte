<script lang="ts">
	import Typography from '../../Typography/typography.svelte';
	import AnimatedShape from './AnimatedShape.svelte';

	let name = 'Glen Chan-Choong';
</script>

<div
	class="bg-gray-50 w-full h-screen relative flex flex-col items-center justify-center snap-section"
>
	<div>
		<div class="flex text-[#3589FF] text-center items-center overflow-hidden pb-2">
			<div class="name flex flex-col w-full items-center text-center">
				<Typography type="heading" as="h1">{name.toUpperCase()}</Typography>
				<Typography type="paragraph" class="name w-[55%]" as="p">
					Hi, I’m {name}— a Toronto-based Graphic Designer with a passion for storytelling and a
					sharp eye for detail. I’ve crafted visual identities, led creative projects, and brought
					ideas to life through bold, effective design.
				</Typography>
			</div>
			<!-- <ul class="list-none flex flex-row gap-[40px]">
				<a href="#">ITEM 1</a>
				<a href="#">ITEM 2</a>
				<a href="#">ITEM 3</a>
			</ul> -->
		</div>
	</div>

	<!-- random shapes in the background of hero section -->
	<div class="hidden md:block">
		<AnimatedShape
			shape="circle"
			color="#3a5780"
			animation="updown"
			size={128}
			className="absolute top-10 left-80 bg-gradient-to-t from-[#3589FF] to-[#3a5780]"
		/>
		<AnimatedShape
			shape="square"
			color="#3a5780"
			animation="rotate"
			size={100}
			className="absolute top-80 right-60"
		/>
		<AnimatedShape
			shape="square"
			color="#3a5780"
			animation="rotate"
			size={62}
			className="absolute bottom-40 left-[30%]"
		/>
	</div>

	<!-- chevron down svg -->
	<svg
		xmlns="http://www.w3.org/2000/svg"
		viewBox="0 0 24 24"
		fill="currentColor"
		class="w-6 h-6 animate-bounce absolute bottom-10 text-[#3589FF]"
	>
		<path
			fill-rule="evenodd"
			d="M12 3.75a.75.75 0 01.75.75v6.75h6.75a.75.75 0 010 1.5H13.5v6.75a.75.75 0 01-1.5 0V14.5H6.75a.75.75 0 010-1.5h6.75V4.5a.75.75 0 01.75-.75z"
			clip-rule="evenodd"
		/>
	</svg>
</div>
