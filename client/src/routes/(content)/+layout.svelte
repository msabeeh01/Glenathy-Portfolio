<!-- FILEPATH: /D:/Fall Semester 2023/Portfolio Projects/Glenathy-Portfolio/client/src/routes/_layout.svelte -->

<script>
	import { page } from '$app/stores';
	import '../../app.css';


	export let title = 'Glen Chan-Choong';
	let isNavOpen = false;

function toggleNav() {
  isNavOpen = !isNavOpen;
}

</script>

<!-- navbar for everything but landing page -->
{#if $page.url.pathname !== '/'}
  <header class="flex w-full justify-between bg-[#2C3950] text-[#F7D5B1] p-4">
    <a href="/">
      <h1 class="text-3xl font-bold transition-all hover:scale-105">{title}</h1>
    </a>
    <nav class="font-bold hidden md:flex">
      <div class="flex gap-5 md:flex">
        <a class="hover:bg-white text-[#F7D5B1] transition hover:text-black rounded-md px-2 py-1" href="/" class:active={$page.url.pathname === '/'}
          >Home</a
        >
        <a
          class="hover:bg-white text-[#F7D5B1] transition hover:text-black rounded-md px-2 py-1"
          href="/about"
          class:active={$page.url.pathname === '/about'}
          >About</a
        >
        <a
          class="hover:bg-white text-[#F7D5B1] transition hover:text-black rounded-md px-2 py-1"
          href="/work"
          class:active={$page.url.pathname === '/work'}
          >Design</a
        >
        <a
          class="hover:bg-white text-[#F7D5B1] transition hover:text-black rounded-md px-2 py-1"
          href="/media"
          class:active={$page.url.pathname === '/media'}>Photography and Video</a
        >
      </div>
    </nav>
    <button class="block md:hidden" on:click={toggleNav}>
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0  0  24  24" stroke="currentColor" class="h-6 w-6 text-gray-500">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4  6h16M4  12h16M4  18h16" />
      </svg>
    </button>
  </header>
  {#if isNavOpen}
    <nav class="flex flex-col w-full md:hidden">
      <a class="block px-2 py-1 text-sm text-white bg-gray-900 rounded-md hover:bg-gray-700" href="/">Home</a>
      <a class="block px-2 py-1 text-sm text-white bg-gray-900 rounded-md hover:bg-gray-700" href="/about">About</a>
      <a class="block px-2 py-1 text-sm text-white bg-gray-900 rounded-md hover:bg-gray-700" href="/work">Design</a>
      <a class="block px-2 py-1 text-sm text-white bg-gray-900 rounded-md hover:bg-gray-700" href="/media">Photography and Video</a>
    </nav>
  {/if}
{/if}

<main class="flex flex-col h-full items-center w-full md:w-2/3 p-4">
	<slot />
</main>


<style>
	.active {
		color: #F7D5B1;
	}




</style>
