<!-- FILEPATH: /D:/Fall Semester 2023/Portfolio Projects/Glenathy-Portfolio/client/src/routes/_layout.svelte -->

<script>
	export let title = 'My Website';
</script>

<!-- <header>
	<h1>{title}</h1>
	<nav>
		<ul>
			<li><a href="/">Home</a></li>
			<li><a href="/about">About</a></li>
			<li><a href="/contact">Contact</a></li>
		</ul>
	</nav>
</header> -->

<main class="container">
	<slot />
</main>

<!-- <footer>
	<p>&copy; {new Date().getFullYear()} My Website</p>
</footer> -->

<style>
	.container {
		background-color: #E6E9D3;
        display:flex;
    	height: 100vh;
	}

	/* Add your CSS styles here */
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
		background-color: #333;
		color: #fff;
	}

	nav ul {
		display: flex;
		list-style: none;
		margin: 0;
		padding: 0;
	}

	nav li {
		margin-right: 1rem;
	}

	nav a {
		color: #fff;
		text-decoration: none;
	}

	main {
	}

	footer {
		padding: 1rem;
		background-color: #333;
		color: #fff;
		text-align: center;
	}
</style>
