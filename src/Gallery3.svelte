<script>
    // You can add props here if needed, e.g.:
    // export let images = [];
  
    const images = [
      { src: "../Svelte-img/LittleDudeGlow.png", alt: "arcane2" },
      { src: "../Svelte-img/RenderSwordHolding.png", alt: "sword" },
      { src: "../Svelte-img/SlyCooperStaffDisplay.png", alt: "staff" },
      { src: "../Svelte-img/CubeMess.png", alt: "cube" },
      { src: "../Svelte-img/CubeThingy.png", alt: "cube2" },
      { src: "../Svelte-img/Cube_Thing_on_Mars.jpg", alt: "cube3" },
    ];
  
    
  </script>
  
  <div class="gallery">
    <h2>Some Blender Projects</h2>
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
      height: 300px;
      border-radius: 4px;
    }
  </style>