<script>
	import '../app.css';
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

	import parking from '$lib/digital_images/film_images/parking.png';

	onMount(() => {
		AOS.init();
	});
	let name = 'Glen Chan-Choong';
</script>

<!-- children should be same width -->
<div class="flex md:flex-row h-screen flex-col-reverse">
	<div data-aos="fade-right" class="text w-full h-full">
		<p class="">{name}</p>

		<Button text="Enter" link="/work" />

		<div class="iconButtonWrapper">
			<IconButton link="https://www.linkedin.com/in/glen-chan-choong-59bb4a1a8/">
				<IoLogoLinkedin />
			</IconButton>

			<IconButton link="https://www.instagram.com/hakka.designs/">
				<IoLogoInstagram />
			</IconButton>

			<!-- <a href="mailto:3JWpF@example.com">
				<IconButton link="https://www.instagram.com/glenchanchoong/">
					<IoIosMail />
				</IconButton>
			</a> -->
		</div>
	</div>

	<div data-aos="fade-left" class="image w-full h-full">
		<img alt="donut and coffee place" src={parking} />
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

	/* make the text responsive */
	@media screen and (max-width: 600px) {
		p {
			font-size: 30px;
		}
	}

	.image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
