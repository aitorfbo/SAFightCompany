<template>
  <header class="header">
    <div class="header-left">
      <h1>Entrena, compite y supérate. inscríbete con nosotros.</h1>
      <p> El momento es ahora. Deja atrás la rutina, despierta tu energía y entrena con nosotros. Supera tus miedos, fortalece tu mente y vive las artes marciales como un estilo de vida.</p>

    </div>
    <div class="header-right">
    <img src="../assets/header.jpg" alt="Header Image" />
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.header {
    padding-top: 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 60rem; /* Set a fixed height for the header */
  color: white;
  overflow: hidden; /* Ensure content doesn't overflow the header */
  text-transform: uppercase;
}

.header-left {
  width: 50%; /* Occupy exactly 50% of the width */
  
  align-self: left;
  color: var(--white);
  letter-spacing: -2px;
  margin-left: 2rem;

  display: column;
  align-items: center;
  font-size: 32px;
  line-height: 1.2;
}

.header-left h1 {
    border-left: 8px solid red;
    padding-left: 12px;
    width: 60%;;
  margin: 0;
}

.header-left p {
  margin: 0;
  font-size: 20px;
  margin-top: 1rem;
  letter-spacing: 0.5px;
  width: 60%;
}

.header-right {
  width: 50%; /* Occupy exactly 50% of the width */
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden; /* Hide any overflow from the image */
}

.header-right img {
  width: 100%; /* Make the image fill the container's width */
  height: 100%; /* Make the image fill the container's height */
  object-fit: cover; /* Crop the image to fit the container */
}
</style>