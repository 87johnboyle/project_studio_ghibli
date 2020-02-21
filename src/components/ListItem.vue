<template lang="html">
  <li v-on:click="handleClick">{{film.title}}</li>
</template>

<script>
import { eventBus } from '../main.js'
export default {

  name:'list-item',
  props: [ 'film' ],
  methods:{
    handleClick(){
      eventBus$emit('film-selected', this.film)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
