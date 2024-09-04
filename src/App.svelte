<script>
  import Gallery from './Gallery.svelte';
  import Gallery2 from './Gallery2.svelte';
  import Gallery3 from './Gallery3.svelte';
  
  let showGallery = false;

  function toggleGallery() {
    showGallery = !showGallery;
  }
</script>

<main>
  <h1>Welcome to a Gallery of a random selection of my projects</h1>
  
  <button on:click={toggleGallery}>
    {showGallery ? 'Remove Gallery' : 'Add Gallery'}
  </button>

  {#if showGallery}
    <Gallery />
  {/if}

  {#if showGallery}
    <Gallery2 />
  {/if}

  {#if showGallery}
  <Gallery3 />
{/if}

</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ffffff;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  button {
    font-size: 1em;
    padding: 10px 20px;
    margin: 20px 0;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  button:hover {
    background-color: #45a049;
  }
</style>