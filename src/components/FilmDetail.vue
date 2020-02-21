<template lang="html">
  <div v-if="film" id="filmDetail">
        <div id="detailWrapper">
          <h2>{{film.title}}</h2>
          <div id="flexWrapper">
            <div id="left">
              <p><span>Description</span>: {{film.description}}</p>
              <p><span>Director</span>: {{film.director}}</p>
              <p><span>Release Date {{film.release_date}}</span></p>
            </div>
          </div>
        </div>
      </div>
</template>

<script>
export default {
  name: "film-detail",
  props: ['film']
}
</script>

<style lang="css" scoped>
</style>
