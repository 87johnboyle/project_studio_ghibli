<template lang="html">
  <select id="films" v-if="films" v-model ="selectedFilm" v-on:change = "handleSelect">
    <option disabled value="">Select a film</option>
        <option v-for="(film, index) in films" :value="film" :key="index">{{ film.title }}</option>
      </select>
</template>

<script>
import {eventBus} from '../main.js'
import ListItem from './ListItem.vue'
export default {
  name: 'films-list',

  data(){
    return {
      selectedFilm: null
    }
  },
  props:['films'],
  components: {
    "list-item": ListItem
  },
  methods: {
    handleSelect(event){
      eventBus.$emit('film-selected', this.selectedFilm);
    }
  }
}
</script>

<style lang="css" scoped>
</style>
