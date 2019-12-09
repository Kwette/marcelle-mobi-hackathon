
<template>
  <div class="container-show">
    <header>
      <button style="position: fixed; top:110px" type="button" class="btn btn-primary hover">
        <a
          style="color: white; font-size: 0.8em"
          :href="movie.trajet"
          target="_blank"
        >Voir sur la carte</a>
      </button>
    </header>
    <h1 class="d-flex flex-column align-items-center">
      {{movie.title}}
      <span style="font-size: 0.4em">({{movie[ "Date de sortie"]}})</span>
    </h1>
    <div class="movie-credits d-flex flex-column justify-content-start align-items-center">
      <p>
        Produit par
        <span>{{movie["Produit Par"]}}</span>
      </p>
      <p>
        Réalisateur
        <span>{{movie["Réalisé par"]}}</span>
      </p>
      <p>
        Principaux interprètes
        <span>{{movie["Principaux Interprétes"]}}</span>
      </p>
      <img v-bind:src="movie.Affiche" />

      <p id="synopsis">{{movie["Synopsis"]}}</p>
    </div>
  </div>
</template>

<script>
import movies from '~/static/movies_json.json'

export default {
  data() {
    return {
      movie: {}
    }
  },
  mounted() {
    // Aller chercher le movie avec cet id
    console.log(parseInt(this.$route.params.id))

    const movie = movies.find(
      movie => movie.id === parseInt(this.$route.params.id)
    )
    this.movie = movie
  }
}
</script>

<style lang="scss">
.container-show {
  margin-top: 4em;
  color: white;
}
.container-show span {
  margin-bottom: 4em;
}
.movie-credits p {
  font-size: 0.8em;
  margin-bottom: 2em;
}
.movie-credits span {
  background-color: #165da4;
  padding: 0.7em;
  border-radius: 4px;
  font-size: 0.8em;
  margin-bottom: 1em;
}
.container-show h1 {
  font-weight: 300;
}
.container-show img {
  width: 70%;
}

p#synopsis {
  margin: 2em 5em;
  text-align: justify;
}

.hover a:hover {
  text-decoration: none;
}

/* -------------- MEDIA QUERIES ----------- */

/* Smartphones (portrait and landscape) ----------- */
@media only screen and (min-device-width: 320px) and (max-device-width: 480px) {
  .container-show img {
    width: 50vw;
  }
  .movie-credits p {
    font-size: 1em;
  }

  .container-show h1 {
    font-size: 2.5em;
  }
  p#synopsis {
    width: 50vw;
    text-align: justify;
  }
}

/* Smartphones (landscape) ----------- */
@media only screen and (min-width: 321px) {
  .container-show img {
    width: 70vw;
  }
  p#synopsis {
    width: 70vw;
    text-align: justify;
  }
}

/* iPads (portrait and landscape) ----------- */
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) {
  .container-show img {
    width: 50vw;
  }
  .movie-credits p {
    font-size: 1em;
  }

  .container-show h1 {
    font-size: 2.5em;
  }
  p#synopsis {
    width: 50vw;
    text-align: justify;
  }
}

/* iPads (landscape) ----------- */
@media only screen and (min-device-width: 900px) and (max-device-width: 1000px) and (orientation: landscape) {
  .container-show img {
    width: 50vw;
  }
  .movie-credits p {
    font-size: 1em;
  }

  .container-show h1 {
    font-size: 2.5em;
  }
  p#synopsis {
    width: 50vw;
    text-align: justify;
  }
}

/* Desktops and laptops ----------- */
@media only screen and (min-width: 1001px) {
  .container-show img {
    width: 50vw;
  }
  .movie-credits p {
    font-size: 1em;
  }

  .container-show h1 {
    font-size: 2.5em;
  }
  p#synopsis {
    width: 50vw;
    text-align: justify;
    width: 50%;
  }
}

/* Large screens ----------- */
@media only screen and (min-width: 1824px) {
  .container-show img {
    width: 50vw;
  }
  .movie-credits p {
    font-size: 1em;
  }

  .container-show h1 {
    font-size: 2.5em;
  }
  p#synopsis {
    width: 50vw;
    text-align: justify;
  }
}
</style>
