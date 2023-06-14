<template>
  <div id="app">
    <MiCatalogo :peliculas="peliculas"></MiCatalogo>
  </div>
</template>

<script>
import MiCatalogo from './components/MiCatalogo.vue';

export default {
  name: 'App',
  components: {
    MiCatalogo
  },
  data() {
    return {
      peliculas: [
        {
          id: 1,
          imagen: './assets/titanik.jpg',
          titulo: 'Titanic',
          duracion: '3h 14m',
          genero: 'Romance, Drama',
          director: 'James Cameron'
        },
        {
          id: 2,
          imagen: './assets/theshaws.jpg',
          titulo: 'The Shawshank Redemption',
          duracion: '2h 22m',
          genero: 'Drama, Crime',
          director: 'Frank Darabont'
        },
        {
          id: 3,
          imagen: './assets/godfather.jpg',
          titulo: 'The Godfather',
          duracion: '2h 55m',
          genero: 'Crime, Drama',
          director: 'Francis Ford Coppola'
        },
        {
          id: 4,
          imagen: './assets/pulfiction.jpg',
          titulo: 'Pulp Fiction',
          duracion: '2h 34m',
          genero: 'Crime, Drama',
          director: 'Quentin Tarantino'
        },
      ]
    };
  }
}
</script>

