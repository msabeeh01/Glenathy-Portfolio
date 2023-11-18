<!-- FILEPATH: /D:/Fall Semester 2023/Portfolio Projects/Glenathy-Portfolio/client/src/routes/_layout.svelte -->

<script>
	import { page } from '$app/stores';
	import '../app.css'

	export let title = 'Glen Chan-Choong';
	
	let showMenu = false;
	function toggleMenu() {
		showMenu = !showMenu;
	}
</script>

<!-- navbar for everything but landing page -->
{#if $page.url.pathname !== '/'}
	<header>
		<h1>{title}</h1>
		<nav>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<div class="hamburger-menu" on:click={toggleMenu} role="button" tabindex="0">
				<div><a href="/" tabindex="0" class:active={$page.url.pathname === '/'}>Home</a></div>
				<div><a href="/about" tabindex="0" class:active={$page.url.pathname === '/about'}>About</a></div>
				<div><a href="/work" tabindex="0" class:active={$page.url.pathname === '/work'}>Design</a></div>
				<div><a href="/contact" tabindex="0" class:active={$page.url.pathname === '/contact'}>Contact</a></div>
				<div><a href="/media" tabindex="0" class:active={$page.url.pathname === '/media'}>Photography and Video</a></div>
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
		height: 100vh;
		justify-content: center;
	}

	.active{
		color:black
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

	.hamburger-menu{
		display: flex;
		flex-direction: row;
		gap:2rem;
	}
	

	nav a {
		color: #BBBBBB;
		text-decoration: none;
		font-size: 30px;
	}

	footer {
		padding: 1rem;
		background-color: #333;
		color: #fff;
		text-align: center;
	}
</style>
