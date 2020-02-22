<template lang="html">
  <div>
    <div class="main-container">
      <films-list :films='films'></films-list>
      <film-detail :film='selectedFilm'></film-detail>
    </div>
  </div>
</template>

<script>
import FilmsList from './components/FilmsList.vue';
import { eventBus } from './main.js';
import FilmDetail from './components/FilmDetail.vue'

export default {
  name: 'app',
  data(){
    return {
      films: [],
      selectedFilm: null
    };
  },
  mounted(){
    fetch('https://ghibliapi.herokuapp.com/films/')
    .then(res => res.json())
    .then(films => this.films = films)

    eventBus.$on('film-selected', (film) => {
      this.selectedFilm = film;
    })
  },
  components:{
    "films-list": FilmsList,
    "film-detail": FilmDetail
  }
}
</script>

<style lang="css" scoped>

</style>
