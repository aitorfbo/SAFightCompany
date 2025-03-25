<template>
    <div class="review-section">
      <!-- Row for YouTube Videos -->
      <div class="video-row">
        <iframe
          class="video"
          src="https://www.youtube.com/embed/aXbUpWq-scY"
          title="YouTube video"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
        <iframe
          class="video"
          src="https://www.youtube.com/embed/wQ_0tGCciQY"
          title="YouTube video"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
        <iframe
          class="video"
          src="https://www.youtube.com/embed/FZRW-xcnU9A"
          title="YouTube video"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
        <iframe
          class="video"
          src="https://www.youtube.com/embed/YlXZW7gLxDY"
          title="YouTube video"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
  
      <!-- Carousel de reseñas de Google -->
      <div class="carousel-container review-carousel">
        <div class="slides">
          <!-- Se duplica el array para un efecto infinito -->
          <div class="slide" v-for="(review, index) in duplicatedReviews" :key="index">
            <div class="review">
              <h3>
                {{ review.name }} <span>{{ review.rating }}</span>
              </h3>
              <p>{{ review.text }}</p>
              <small>{{ review.time }}</small>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Review",
    data() {
      return {
        reviews: [
          {
            name: "Benjamin Gabancho",
            rating: "5/5",
            text:
              "Un gimnasio con un ambiente increíble y perfecto para aprender BJJ y Grappling. Sebas se lo curra cada día, con gran experiencia y se adapta al 100% de las personas que entrenamos allí. ¡Totalmente recomendable!",
            time: "Hace 8 meses"
          },
          {
            name: "Alazne Ayala",
            rating: "5/5",
            text:
              "Gimnasio 100% recomendable. Tanto Andy en judo como Sebas y Adri en BJJ son unos profesores top. Tanto si empiezas desde 0 como si vienes de otros gimnasios, lo recomendaría sin lugar a dudas.",
            time: "Hace un año"
          },
          {
            name: "Alex Molero Lebrero",
            rating: "5/5",
            text:
              "Ambiente extraordinario para empezar en el mundo de las artes marciales, profes excelentes y compañeros siempre dispuestos a ayudarte. ¡Un auténtico lujo estar rodeado de todos!",
            time: "Hace un año"
          },
          {
            name: "Mateo Rivera",
            rating: "5/5",
            text:
              "El ambiente de entreno es brutal pues hay una competencia de alto rigor pero de cuidado entre compañeros. Cada clase tiene un altísimo nivel técnico aplicado a…",
            time: "Hace 3 años"
          },
          {
            name: "Asier Velasco Salgueiros",
            rating: "5/5",
            text:
              "Gimnasio con instalaciones nuevas, los profesores Adri y Sebas siempre enseñando todo lo que saben para que sus alumnos mejoren.…",
            time: "Hace 3 años"
          },
          {
            name: "keyser sozek",
            rating: "5/5",
            text:
              "Después de casi un año en este gimnasio puedo asegurar que el ambiente es el más apropiado para formarse en el arte del brazilian jiu-jitsu y el grappling.",
            time: "Hace un año"
          },
          {
            name: "Ander Conal Fuertes",
            rating: "5/5",
            text:
              "Profesor de calidad, atento y trabajador. Ni un milímetro a la improvisación, tanto para iniciarte como para avanzado/competición. Dedicación absoluta.",
            time: "Hace 7 años"
          },
          {
            name: "Eva Rodríguez García",
            rating: "5/5",
            text:
              "Mi centro de entrenamiento ya casi desde hace dos años, ahora nos hemos mudado a este nuevo centro y es brutal! En pocos días ya hemos vuelto a darle ese impulso.",
            time: "Hace 3 años"
          }
        ]
      }
    },
    computed: {
      duplicatedReviews() {
        // Duplica el array para el efecto infinito
        return [...this.reviews, ...this.reviews];
      }
    }
  };
  </script>
  
  <style scoped>
  .review-section {
    padding: 8rem 2rem;
    background-color: black; /* Fondo oscuro */
    color: var(--white);
    display: flex;
    flex-direction: column;
    gap: 5rem;
  }
  
  /* Estilos para la fila de videos */
  .video-row {
    display: flex;
    justify-content: space-between;
    gap: 1rem;
  }
  
  .video {
    width: 23%; /* Cuatro videos en una fila */
    height: 15rem;
    border: 2px solid red;
  }
  
  /* Estilos para el carrusel de reseñas */
  .carousel-container.review-carousel {
    overflow: hidden;
    position: relative;
    width: 100%;
  }
  
  .slides {
    display: flex;
    animation: scroll 20s linear infinite;
  }
  
  .slide {

    min-width: 25%; /* Se muestran 4 recuadros a la vez */
    box-sizing: border-box;
    padding: 2rem;
  }
  
  /* Fixed-size review boxes with larger text */
  .review {
    padding-top: 2rem;
    background: rgba(255, 255, 255, 0.9); /* Fondo semitransparente */
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    text-align: center;
    color: #333; /* Texto oscuro para contraste */
    height: 150px; /* All boxes have the same minimum height */
  }
  
  .review h3 {
    margin: 0 0 10px;
    font-size: 1.25rem; /* Increased text size */
  }
  
  .review h3 span {
    font-weight: normal;
    font-size: 1rem; /* Increased rating text size */
    margin-left: 0.5rem;
    color: #f5333f;
  }
  
  .review p {
    margin: 0 0 10px;
    font-size: 1rem; /* Larger comment text */
    line-height: 1.4;
  }
  
  .review small {
    display: block;
    color: #666;
    font-size: 0.85rem; /* Larger date text */
  }
  
  /* Animación para scroll infinito */
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%);
    }
  }
  </style>
  