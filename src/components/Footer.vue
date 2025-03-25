<template>
    <footer class="site-footer">
      <!-- Background overlay with inverted image -->
       <div class="grey-overlay"></div>
      <div
        class="footer-bg"
        :style="{ backgroundImage: 'url(' + footerImage + ')' }"
      ></div>
  
      <!-- Footer content -->
      <div class="footer-content">
        <!-- Logo / Title -->

        <!-- Main footer links -->
        <div class="footer-links">
          <div class="links-column">
            <h4>CLASSES</h4>
            <ul>
              <li><a href="#">MMA</a></li>
              <li><a href="#">Muay Thai</a></li>
              <li><a href="#">Brazilian Jiu Jitsu</a></li>
              <li><a href="#">Boxing</a></li>
              <li><a href="#">Kids Classes</a></li>
              <li><a href="#">Personal Training</a></li>
            </ul>
          </div>
          <div class="links-column">
            <h4>INFO</h4>
            <ul>
              <li><a href="#">Schedule</a></li>
              <li><a href="#">Gym Etiquette</a></li>
              <li><a href="#">FAQ</a></li>
              <li><a href="#">History</a></li>
              <li><a href="#">Installations</a></li>
              <li><a href="#">Free Pass</a></li>
            </ul>
          </div>
          <div class="links-column">
            <h4>STORE</h4>
            <ul>
              <li><a href="#">Shipping</a></li>
              <li><a href="#">Returns</a></li>
              <li><a href="#">Privacy Policy</a></li>
              <li><a href="#">Terms</a></li>
              <li><a href="#">Contact</a></li>
            </ul>
          </div>
        </div>
  
        <!-- Footer bottom / Credits -->
        <div class="footer-bottom">
          <p>
            Copyright © 2023 |
            Designed by Kalambre Studio |
            Powered by Vue
          </p>
          <p>
            <a href="#">User Guide</a> |
            <a href="#">Style Guide</a> |
            <a href="#">Licenses</a> |
            <a href="#">Changelog</a>
          </p>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  // Using a relative path since Footer.vue is in src/components:
  import footerImage from '../assets/footer.jpg';
  
  export default {
    name: 'SiteFooter',
    data() {
      return {
        footerImage
      };
    }
  };
  </script>
  
  <style scoped>
  .site-footer {
    z-index: 1000  !important;
    position: relative;
    width: 100%;
    min-height: 400px;
    color: #fff;
    overflow: hidden;
  }

  .grey-overlay {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 1000;
  }
  
  /* Background overlay with the inverted image */
  .footer-bg {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    filter: invert(1);
    z-index: 0;
  }
  
  /* Actual footer content in front of the background */
  .footer-content {
    
    position: relative;
    z-index: 1;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 100000;
  }
  
  /* Logo / Title area */
  .footer-logo-wrap {
    margin-bottom: 1rem;
  }
  .footer-logo {
    max-width: 180px;
  }
  
  /* Main links area */
  .footer-links {
    
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10rem;
    margin-bottom: 2rem;

  }
  .links-column h4 {
    
    margin-bottom: 0.5rem;
    font-size: 1.1rem;
    text-transform: uppercase;
  }
  .links-column ul {
    
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .links-column li {
    margin-bottom: 0.5rem;
  }
  .links-column a {
    color: #fff;
    text-decoration: none;
  }
  .links-column a:hover {
    text-decoration: underline;
  }
  
  /* Bottom credits area */
  .footer-bottom {
    text-align: center;
    font-size: 0.85rem;
    line-height: 1.4;
  }
  .footer-bottom a {
    color: #fff;
    text-decoration: none;
  }
  .footer-bottom a:hover {
    text-decoration: underline;
  }
  </style>
  