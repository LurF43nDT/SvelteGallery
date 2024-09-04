<script>
  import Gallery from './Gallery.svelte';
  import Gallery2 from './Gallery2.svelte';
  import Gallery3 from './Gallery3.svelte';
  
  let showGallery = false;

  function toggleGallery() {
    showGallery = !showGallery;
  }

  let showGallery2 = false;

function toggleGallery2() {
  showGallery2 = !showGallery;
}

let showGallery3 = false;

function toggleGallery3() {
  showGallery3 = !showGallery;
}

</script>

<main>
  
  <h1>Welcome to a Gallery of a random selection of some of my projects</h1>
  
  <button on:click={toggleGallery}>
    {showGallery ? 'Drawings, Yes' : 'Random Drawings'}
  </button>
  
  <button on:click={toggleGallery2}>
    {showGallery2 ? 'IDK' : 'PhotoShop Projects'}
  </button>

  <button on:click={toggleGallery3}>
    {showGallery3 ? 'Stuff' : 'Blender Stuff'}
  </button>

  {#if showGallery}
    <Gallery />
  {/if}

  {#if showGallery2}
    <Gallery2 />
  {/if}

  {#if showGallery3}
  <Gallery3 />
{/if}

</main>

<style>

  main {
    text-align: center;
    padding: 1em;
    max-width: 300px;
    margin:  auto;

  }

  h1 {
    color: #fff201;
    background-color: rgba(0, 0, 0, 0.405);
    font-size: 4em;
    font-weight: 100;
    border-radius: 5em;
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
    background-color: #4caf4fd2;
    color: #fff201;
    border: none;
    border-radius: 4px;
    cursor:no-drop
  }

  button:hover {
    background-color: #010c01;
  }
</style>