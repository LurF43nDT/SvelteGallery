<script>
    // You can add props here if needed, e.g.:
    // export let images = [];
  
    const images = [
      { src: "../Svelte-img/Arcane JuleFilmJpeg2.jpg", alt: "arcane2" },
      { src: "../Svelte-img/Arcane JuleFilmJpeg3.jpg", alt: "arcane3" },
      { src: "../Svelte-img/Clint-Eastwood.png", alt: "FireFart" },
      { src: "../Svelte-img/FHIKrillSnus.png", alt: "krill" },
    ];
  
    
  </script>
  
  <div class="gallery">
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
      max-width: auto;
      height: 450px;
      border-radius: 4px;
    }
  </style>