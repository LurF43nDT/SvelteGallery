<script>
  // You can add props here if needed, e.g.:
  // export let images = [];

  const images = [
    { src: "../Svelte-img/GhoulGirl.png", alt: "Ghoul" },
    { src: "../Svelte-img/GhoulGirl-skateboard.png", alt: "skateboard" },
    { src: "../Svelte-img/abomanation.png", alt: "abomanation" },
    { src: "../Svelte-img/SpiderGate.png", alt: "SpiderGate" },
  ];

  
</script>

<div class="gallery">
  <h2>Some Drawings</h2>
  <div class="image-container">
    {#each images as image}
      <img src={image.src} alt={image.alt} />
    {/each}
  </div>
</div>

<style>
  .gallery {
    margin: 20px;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
  }

  .image-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
  }

  img {
    max-width: 300px;
    height: auto;
    border-radius: 4px;
  }
</style>