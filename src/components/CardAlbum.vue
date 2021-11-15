<template>
    <div class="row" v-if="!loading">
     <div class="col-md-2" v-for="album in albums" :key="album.title">
        <div class="card card_album">
          <img :src="album.poster" alt="album.title">
          <h1>{{album.title}}</h1>
          <p>{{album.author}}</p>
          <p>{{album.year}}</p>
        </div>
   
    </div>
   </div>
   <div class="loading" v-else>LOADING...</div>
</template>

<script>
import axios from "axios";

export default {
 data(){
   return {
     albums: [],
     loading: true,
     API_URL: "https://flynn.boolean.careers/exercises/api/array/music",
   }
 },
  mounted() {
    axios
    .get(this.API_URL)
    .then(r=>{
      this.albums = r.data.response;
      this.loading = false;
    }).catch(e=>{
      console.log(e);
    })

  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/card.scss';
.loading{
  color: red;
  font-size: 30px;
}

</style>
