<script>
	import '../app.css'
	// component imports
	import Button from '$lib/Button/Button.svelte';
	import IconButton from '$lib/IconButton/IconButton.svelte';

	// icons import
	// @ts-ignore
	import IoLogoInstagram from 'svelte-icons/io/IoLogoInstagram.svelte';
	// @ts-ignore
	import IoLogoLinkedin from 'svelte-icons/io/IoLogoLinkedin.svelte';
	// @ts-ignore
	import IoIosMail from 'svelte-icons/io/IoIosMail.svelte';

	import { onMount } from 'svelte';
	import AOS from 'aos';

	onMount(() => {
		AOS.init();
	});
	let name = 'Glen Chan-Choong';
</script>

<!-- children should be same width -->
<div class="flex md:flex-row h-screen flex-col-reverse">
	<div data-aos="fade-right" class="text w-full h-full">
		<p>{name}</p>

		<Button text="Enter" link="/work" />

		<div class="iconButtonWrapper">
			<IconButton link="https://www.instagram.com/glenchanchoong/">
				<IoLogoLinkedin />
			</IconButton>

			<IconButton link="https://www.instagram.com/hakka.designs/">
				<IoLogoInstagram />
			</IconButton>

			<IconButton link="https://www.instagram.com/glenchanchoong/">
				<IoIosMail />
			</IconButton>
		</div>
	</div>

	<div data-aos="fade-left" class="image w-full h-full">
		<img
			alt="donut and coffee place"
			src="https://cdn.myportfolio.com/7bf13fc8-be3c-4bd4-96b0-ae0f57e2689c/5b23af0c-ec60-4c9a-84a6-d873664e0e9b_rwc_0x0x1783x1179x4096.png?h=a702da7ab03e39908a66c52e6fc85ef6"
		/>
	</div>
</div>

<style>
	.iconButtonWrapper {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 15px;
	}

	.text {
		display: flex;
		flex-direction: column;
		text-align: center;
		justify-content: center;
		align-items: center;
		gap: 30px;
	}

	p {
		font-weight: 900;
		font-size: 69px;
		margin: 0;
		font-family: 'Akira', sans-serif;
		/* font-family: "Museo Slab W00 900"; */
		color: #f7d5b1;
	}

	.image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
