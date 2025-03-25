<template>
    <div class="teaser">
      <!-- Transparent grey overlay with text -->
      <div class="teaser-overlay">
        <h2>APRENDE ARTES MARCIALES CON LOS MEJORES DEL MUNDO.</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. Aenean faucibus nibh et justo cursus id rutrum lorem imperdiet. Nunc ut sem vitae risus tristique posuere.</p>
        <div class="botones">
          <a class="in" href="/inscribete">Pase Gratuito</a>
          <a class="co" href="/contacto">Contacto</a>
        </div>
      </div>
      <!-- Image instead of video -->
      <img class="teaser-image" src="../assets/penultimo.png" alt="Teaser Image" />
    </div>
  </template>
  
  <script>
  export default {
    name: "Penultimo",
  };
  </script>
  
  <style scoped>
  .teaser {
    position: relative; /* Enable positioning for overlay */
    width: 100%;
    height: 40rem; /* Fixed height */
    overflow: hidden;
    background-color: red;
  }
  
  /* Overlay styling remains the same */
  .teaser-overlay {
    position: absolute;
    width: 40%;
    height: 70%;
    background-color: rgba(0, 0, 0, 0.8); /* Transparent grey background */
    display: flex;
    top: 12%;
    left: 8rem;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    color: white;
    text-align: left;
    padding: 1rem;
    z-index: 1000;
    border-right: 8px solid red;
  }
  
  .teaser-overlay h2 {
    padding: 1rem;
    font-size: 40px;
  line-height: 1.2;
    margin: 0;
  }
  
  .teaser-overlay p {
    padding-left: 1rem;
    font-size: 20px;
    margin: 0.5rem 0 0;
    line-height: 1.2;
  }
  
  .teaser-overlay div.botones {
    display: flex;
    padding: 1rem;
    gap: 2rem;
    font-size: 20px;
  }
  
  .teaser-overlay a.in {
    border: 2px solid red;
    background-color: red;
    color: white;
    padding: 0.5rem 1rem;
    text-decoration: none;
    margin-top: 1rem;
  }
  
  .teaser-overlay a.co {
    border: 2px solid white;
    color: white;
    padding: 0.5rem 1rem;
    text-decoration: none;
    margin-top: 1rem;
  }
  
  /* Image styling similar to video styling */
  .teaser-image {
    width: 30%;
    height: 100%;
    object-fit: cover;
    right: 10%;
    position: absolute;
    filter: grayscale(100%);
  }
  </style>
  