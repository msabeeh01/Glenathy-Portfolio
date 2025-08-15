<script>
	// @ts-nocheck
	/** @type {{img: any, title?: string, height?: number}} */
	let { img, title = "", height = 400 } = $props();
	let showTitle = $state(false);
	let isModalOpen = $state(false); // Variable to track the modal state

</script>

<div
	class="hover:scale-105 transition-all duration-200 flex group rounded-lg overflow-hidden"
	onmouseover={() => (showTitle = true)}
	onmouseout={() => (showTitle = false)}
	onfocus={() => (showTitle = true)}
	onblur={() => (showTitle = false)}
	role="button"
	tabindex="0"
>
	<div class="flex flex-col w-full justify-center">
		<button onclick={() => (isModalOpen = !isModalOpen)} class="">
			<picture>
				<img class="rounded-lg object-cover w-full" style="height: {height}px;" src={img} alt="" />
			</picture>
		</button>
		{#if showTitle && title != ""}
			<div
				class="text-center w-full absolute bottom-0 left-0 p-2 rounded shadow-lg opacity-0 group-hover:opacity-100 transition-opacity duration-200 bg-gradient-to-r from-black via-black to-transparent backdrop-filter backdrop-blur-md"
			>
				<p class="text-sm font-light text-white">
					{title}
				</p>
			</div>
		{/if}
	</div>
</div>

<!-- Modal -->
{#if isModalOpen}
	<button
		class="modal"
		onclick={() => (isModalOpen = false)}
		onkeydown={(e) => {
			if (e.key === 'Escape') isModalOpen = false;
		}}
		aria-labelledby="modalTitle"
		tabindex="0"
	>
		<img class="modal-image" src={img} alt="" />
	</button>
{/if}

<style>
	/* Add styles for the modal */
	.modal {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.8);
		display: flex;
		justify-content: center;
		align-items: center;
		z-index: 1000;
	}

	.modal-image {
		max-width: 90%;
		max-height: 90%;
	}
</style>
