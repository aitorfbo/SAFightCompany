<template>
    <nav class="navbar">
      <!-- Lado izquierdo: Marca -->
      <div class="navbar-brand">
        <span class="brand-sa">SA</span>
        <span class="brand-fight">FIGHT COMPANY</span>
      </div>
      <!-- Lado derecho: Links -->
      <ul class="navbar-links">
        <li><a href="/nuestr-equipo">NUESTRO EQUIPO</a></li>
        <li><a href="/clases">CLASES</a></li>
        <li><a href="/eventos">EVENTOS</a></li>
        <li><a href="/contacto">CONTACTO</a></li> 
        <li><a href="/info">INFO</a></li>
        <li><a class="inc" href="/inscribete">INSCRÍBETE</a></li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    name: "Navbar",
  };
  </script>
  
  <style scoped>

  .navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 2rem;
  }
  
  .navbar-brand {
    display: flex;
    align-items: center;
    font-size: 32px;
    font-weight: bold;
  }
  
  .brand-sa {
    color: red;
    margin-right: 0.5rem;
  }
  
  .brand-fight {
    color: white; 
  }
  
  .navbar-links {
    list-style: none;
    display: flex;
    gap: 2rem;
    font-size: 20px
  }
  
  .navbar-links li a {
    color: white;
    text-decoration: none;
  }

  .navbar-links li a.inc {
    background-color: red;
    padding: 0.5rem;
  }
  </style>
  