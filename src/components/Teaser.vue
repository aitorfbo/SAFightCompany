<template>
  <div class="teaser">
    <!-- Transparent grey box with text -->
    <div class="teaser-overlay">
      <h2>Entrena con nosotros</h2>
      <p>Descubre tu potencial y vive las artes marciales, solicita tu pase para un entrenamiento gratuito</p>
      <div class="botones">
        <a class="in" href="/inscribete">Pase Gratuito</a>
        <a class="co" href="/contacto">Contacto</a>
      </div>
    </div>
    <!-- Video -->
    <video class="teaser-video" autoplay loop muted>
      <source src="../assets/teaser.mp4" type="video/mp4" />
    </video>
  </div>
</template>

<script>
export default {
  name: "Teaser",
};
</script>

<style scoped>
.teaser {
  position: relative; /* Enable positioning for overlay */
  width: 100%;
  height: 40rem; /* Limited height */
  overflow: hidden;
}

.teaser-overlay {
  position: absolute; /* Position the overlay on top of the video */
  width: 20%;
  height: 32%; /* Cover the entire teaser container */
  background-color: rgba(0, 0, 0, 0.5); /* Transparent grey background */
  display: flex;
  top: 35%;
  right: 8rem;
  flex-direction: column;
  align-items: left;
  justify-content: center;
  color: white; /* Text color */
  text-align: left;
  align-self: right;
  padding: 1rem;
  z-index: 1000;
  border-right: 8px solid red;

}

.teaser-overlay h2 {
    padding: 1rem;
  font-size: 32px;
  margin: 0;
}

.teaser-overlay p {
padding-left: 1rem;
  font-size: 1.2rem;
  margin: 0.5rem 0 0;
  font-size: 20px;
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

.teaser-video {
  width: 100%; /* Make the video fill the width */
  height: 100%; /* Make the video fill the height */
  object-fit: cover; /* Crop the video to fit the container */
  filter: grayscale(100%);
}
</style>