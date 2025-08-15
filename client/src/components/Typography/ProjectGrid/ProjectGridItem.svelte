<script lang="ts">

	interface ProjectItem {
		src: string;
		desc: string;
	}

	let { item }: { item: ProjectItem } = $props();

</script>

{#if item}
	<a
		href="#"
		class="relative aspect-square w-full lg:max-w-[400px] bg-black group flex items-center justify-center projectitem"
	>
		<img src={item.src} alt="" class="h-full w-full object-cover" />
		<div
			class="absolute inset-0 flex text-white font-extrabold justify-center items-center bg-[#3589FF] opacity-0 group-hover:opacity-90 transition-opacity duration-300 pointer-events-none"
		>
			{item.desc}
		</div>
	</a>
{/if}
