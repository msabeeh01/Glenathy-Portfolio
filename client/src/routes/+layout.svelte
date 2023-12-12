<!-- FILEPATH: /D:/Fall Semester 2023/Portfolio Projects/Glenathy-Portfolio/client/src/routes/_layout.svelte -->

<script>
	import { page } from '$app/stores';
	import '../app.css';

	export let title = 'Glen Chan-Choong';

</script>

<!-- navbar for everything but landing page -->
{#if $page.url.pathname !== '/'}
	<header class="flex">
		<h1 class="text-3xl font-bold">{title}</h1>
		<nav class="font-bold">
			<div class="flex gap-5" >
				<a class="hover:bg-white text-[#bbbbbb] transition hover:text-black rounded-md px-2 py-1" href="/" class:active={$page.url.pathname === '/'}
					>Home</a
				>
				<a	
				class="hover:bg-white text-[#bbbbbb] transition hover:text-black rounded-md px-2 py-1"
					href="/about"
					class:active={$page.url.pathname === '/about'}
					>About</a
				>
				<a
				class="hover:bg-white text-[#bbbbbb] transition hover:text-black rounded-md px-2 py-1"
					href="/work"
					class:active={$page.url.pathname === '/work'}
					>Design</a
				>
				<a
				class="hover:bg-white text-[#bbbbbb] transition hover:text-black rounded-md px-2 py-1"
					href="/media"
					class:active={$page.url.pathname === '/media'}>Photography and Video</a
				>
			</div>
		</nav>
	</header>
{/if}

<main class="pageCon">
	<slot />
</main>

<!-- <footer>
	<p>&copy; {new Date().getFullYear()} My Website</p>
</footer> -->

<style>
	.pageCon {
		background-color: white;
		display: flex;
		flex-direction: column;
		align-items: center;
		height: 100%;
	}

	.pageCon > *{
		margin-top: auto;
		margin-bottom: auto;
	}

	.active {
		color: black;
	}

	/* Add your CSS styles here */
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
		background-color: #fbffe0;
		color: #444444;
	}


	footer {
		padding: 1rem;
		background-color: #333;
		color: #fff;
		text-align: center;
	}


</style>
