<template lang="html">
  <div v-if="film" id="filmDetail">
        <div id="detailWrapper">
          <h2>{{film.title}}</h2>
          <div id="flexWrapper">
            <div id="details">
              <p><span><h3>Description</h3></span> {{film.description}}</p>
              <p><span><h3>Director</h3></span> {{film.director}}</p>
              <p><span><h3>Release Date</h3></span>{{film.release_date}}</p>
              <p><span v-bind:class= "film.rt_score < 50 ? 'red' : 'green'"><h3>RT Score</h3></span><span>{{ film.rt_score }}%</span></p>
            </div>
            <template v-if="film.title === 'Castle in the Sky'">
    <img src="https://images.alphacoders.com/828/thumb-1920-828255.png">
  </template>
  <template v-if="film.title === 'My Neighbor Totoro'">
    <img src="https://i.pinimg.com/originals/c0/45/58/c045589789eccc907c6959a2e7641d54.jpg">
  </template>
  <template v-if="film.title === 'Kikis Delivery Service'">
    <img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fthewellredmage.files.wordpress.com%2F2016%2F12%2Fkiki-pos_1440449334.png%3Fw%3D500&imgrefurl=https%3A%2F%2Fthewellredmage.com%2F2016%2F12%2F11%2Fkikis-delivery-service%2F&docid=Ww8YtVgCpOW-XM&tbnid=Nywkj54DkAkcqM%3A&vet=10ahUKEwjonf-c3dTgAhVuwMQBHZCKAKUQMwioAShNME0..i&w=500&h=750&bih=710&biw=1386&q=Kiki%27s%20Delivery%20Service%20hd&ved=0ahUKEwjonf-c3dTgAhVuwMQBHZCKAKUQMwioAShNME0&iact=mrc&uact=8">
  </template>
  <template v-if="film.title === 'Only Yesterday'">
    <img src="https://ic.c4assets.com/brands/only-yesterday/a88e3d6d-e6e6-4c8d-9b7e-a80a25b1861e.jpg?interpolation=progressive-bicubic&output-quality=90">
  </template>
  <template v-if="film.title === 'Grave of the Fireflies'">
    <img src="https://keithandthemovies.files.wordpress.com/2017/12/graveposter.jpg?w=545">
  </template>
  <template v-if="film.title === 'Porco Rosso'">
    <img src="http://barkerhost.com/wp-content/uploads/sites/4/2016/06/porco-banner.jpg">
  </template>
  <template v-if="film.title === 'Pom Poko'">
    <img src="https://fanart.tv/fanart/movies/15283/hdmovieclearart/pom-poko-54ea2a3f639e1.png">
  </template>
  <template v-if="film.title === 'Whisper of the Heart'">
    <img src="https://m0.joe.co.uk/wp-content/uploads/2018/07/25164315/ce196d896889ce984b8c36f6c8ed64b0.jpg">
  </template>
  <template v-if="film.title === 'Princess Mononoke'">
    <img src="https://backtotheviewer.files.wordpress.com/2015/11/princess-mononoke.jpg?w=640">
  </template>
  <template v-if="film.title === 'My Neighbors the Yamadas'">
    <img src="https://entropymag.org/wp-content/uploads/2015/03/series_1484.jpg">
  </template>
  <template v-if="film.title === 'Spirited Away'">
    <img src="https://cdn.hitc-s.com/i/189/spirited_away_wallpaper_by_behruz_78544.jpg">
  </template>
  <template v-if="film.title === 'The Cat Returns'">
    <img src="https://s1.thcdn.com/productimg/1600/1600/11655841-9754546298583822.jpg">
  </template>
  <template v-if="film.title === 'Tales from Earthsea'">
    <img src="https://filmschoolrejects.com/wp-content/uploads/2018/05/tales-from-earthsea.png">
  </template>
  <template v-if="film.title === 'Ponyo'">
    <img src="http://images2.fanpop.com/image/photos/11000000/Ponyo-ponyo-on-the-cliff-by-the-sea-11063832-1280-1024.jpg">
  </template>
  <template v-if="film.title === 'Arrietty'">
    <img src="https://m.media-amazon.com/images/M/MV5BMTAxNjk3OTYyODReQTJeQWpwZ15BbWU3MDgyODY2OTY@._V1_.jpg">
  </template>
  <template v-if="film.title === 'From Up on Poppy Hill'">
    <img src="https://www.nziff.co.nz/assets/resized/sm/upload/vf/48/ah/ai/Poppy%20Hill%20NEW%20KEY%20c0349_t2JPEG.0082-2000-2000-1125-1125-crop-fill.jpg">
  </template>
  <template v-if="film.title === 'The Wind Rises'">
    <img src="https://i.ytimg.com/vi/RzSpDgiF5y8/maxresdefault.jpg">
  </template>
  <template v-if="film.title === 'The Tale of the Princess Kaguya'">
    <img src="https://cdn-static.denofgeek.com/sites/denofgeek/files/styles/main_wide/public/0/21/kaguya-main.jpg?itok=LIRawTR3">
  </template>
  <template v-if="film.title === 'When Marnie Was There'">
    <img src="https://ic.c4assets.com/bips/when-marnie-was-there/articles/931b0b3a-b75f-40e1-af60-16510f8ec547.jpg?interpolation=progressive-bicubic&output-quality=90">
  </template>
  <template v-if="film.title === `Kiki's Delivery Service`">
    <img src="https://i2.wp.com/thespool.net/wp-content/uploads/2019/04/screen_shot_2019-03-12_at_12.44.08_pm-e1557600864430.png?fit=1024%2C613&ssl=1">
  </template>
<template v-if="film.title === `Howl's Moving Castle`">
  <img src="https://i1.wp.com/thespool.net/wp-content/uploads/2019/04/howl-2.jpg?resize=1024%2C576&ssl=1">
</template>

<!-- <button v-on:click="moreInfo()">More Info</button> -->

<!-- <div id="hide">
<p><span><h3>People</h3></span> {{people.name}}</p>
</div> -->
          </div>
        </div>
      </div>
</template>

<script>
export default {
  name: "film-detail",
  props: ['film'],

methods:{
  mounted(){
  fetch('https://ghibliapi.herokuapp.com/people')
  .then(res => res.json())
  .then(people => this.people = people)
},
  moreInfo() {
  let x = document.getElementById("hide");
  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
}
}
</script>

<style lang="css" scoped>

h2 {
  text-align: center;
  padding: 1.5rem 2.5rem;
  background-image: linear-gradient(120deg, #fbc2eb 0%, #a6c1ee 100%);
  margin: 0 0 2rem 0;
  font-size: 1.5rem;
  color: white;
  border-radius: 25px
}

#filmDetail {
  width: 500px;
  margin: 1rem;
  background: white;
  box-shadow: 2px 4px 25px rgba(0, 0, 0, .1);
  border-radius: 25px;
  overflow: hidden;
  flex-wrap: wrap;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

#details {
  /* padding: 5px; */
  text-align: center;
}

img{
       max-width: 100%;
       max-height: 100%;
       display: block;
   }

.red{
  color:red;
}
.green {
  color:green;
}

</style>
