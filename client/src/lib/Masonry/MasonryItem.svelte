<script>
    export let img;
    export let title;
    let showTitle = false;
  </script>
  
  <div class="hover:scale-105 transition-all duration-200 relative group" on:mouseover={() => showTitle = true} on:mouseout={() => showTitle = false}>
    <button on:click={() => {}}>
        <img height="200" class="rounded-lg object-cover" src={img} alt="">
    </button>
    {#if showTitle}
        <p class="w-full absolute bottom-0 left-0 bg-white p-2 rounded shadow-lg opacity-0 group-hover:opacity-100 transition-opacity duration-200">{title}</p>
    {/if}
 </div>