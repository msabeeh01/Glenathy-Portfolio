<script>
	import '../app.css';
	let name = 'Glen Chan-Choong';

	//array of images and their description
	const imgArray = [
		{
			src: '/digital_images/RY_LOGO_Final_-_Colour_Text_-_png.jpg',
			desc: 'Rosewood Youth Redesign'
		},
		{
			src: '/digital_images/illustrator_images/GCM 320 Proj4 - Chan-Choong Glen-01.png',
			desc: 'Stoicism'
		},
		{
			src: '/digital_images/illustrator_images/Hakka Designs Main-01.jpg',
			desc: 'Hakka Design Logo'
		},
		{
			src: '/digital_images/photoshop_images/Chan-Choong_Glen_Section4_CDCover.jpg',
			desc: 'Memory Album Cover'
		},
		{
			src: '/digital_images/photoshop_images/Chan-Choong_Glen_Section4_LTL.jpg',
			desc: 'Neo Tokyo, Cyberwear'
		}
	];
</script>

<!-- children should be same width -->
<div class="w-screen">
	<!-- Main Container, seperate from page container -->
	<div class="flex flex-col gap-[76px] py-[70px] mx-auto max-w-[1200px] h-full px-[70px]">
		<!-- NAVBAR -->
		<div class="flex justify-between text-[#3589FF] items-center">
			<div class="text-2xl md:text-4xl lg:text-6xl font-extrabold">{name}</div>
			<!-- <ul class="list-none flex flex-row gap-[40px]">
				<a href="#">ITEM 1</a>
				<a href="#">ITEM 2</a>
				<a href="#">ITEM 3</a>
			</ul> -->
		</div>

		<!-- SHORT INFO SECTION -->
		<div class="w-full lg:w-[55%]">
			<h1 class="text-[1.5em] leading-[1.2em]">
				Hi, I’m {name}— a Toronto-based Graphic Designer with a passion for storytelling and a sharp
				eye for detail. I’ve crafted visual identities, led creative projects, and brought ideas to
				life through bold, effective design.
			</h1>
		</div>

		<!-- 3X4 grid (400px X 400px) -->
		<div class="flex flex-col md:grid md:grid-cols-2 lg:grid-cols-3 w-full">
			{#each imgArray as item, index}
				<a
					href="#"
					class="relative aspect-square w-full lg:max-w-[400px] bg-black group flex items-center justify-center"
				>
					<img src={item.src} alt="" class="h-full w-full object-cover" />
					<div
						class="absolute inset-0 flex text-white font-extrabold justify-center items-center bg-[#3589FF] opacity-0 group-hover:opacity-90 transition-opacity duration-300 pointer-events-none"
					>
						{item.desc}
					</div>
				</a>
			{/each}
		</div>
	</div>
</div>
