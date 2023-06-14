<template>
  <table class="table">
    <thead>
      <tr>
        <th>Imagen</th>
        <th>Título</th>
        <th>Duración</th>
        <th>Género</th>
        <th>Director</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="pelicula in peliculas" :key="pelicula.id">
        <td><img :src="pelicula.imagen" :alt="pelicula.titulo" width="150"></td>
        <td>{{ pelicula.titulo }}</td>
        <td>{{ pelicula.duracion }}</td>
        <td>{{ pelicula.genero }}</td>
        <td>{{ pelicula.director }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: 'MiCatalogo',
  props: {
    peliculas: {
      type: Array,
      required: true
    },
  }
}
</script>

<style scoped>

.table {
    width: 100%;
    height: 10px;
    margin-bottom: 1rem;
    font-size: 20px;
    text-align: center;
  }
  
  .table th,
  .table td {
    padding: 0.5rem;
    background-color: black;
    color: white;
  }
  
  .table th {
    background-color: #9d0208;
    font-weight: bold;
    text-align: center;
  }
  
  .table td img {
    max-width: 150px;
    height: auto;
  }
</style>
