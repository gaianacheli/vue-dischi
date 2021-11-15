<template>
    <div class="row">
  <div class="col-md-2" v-for="album in albums" :key="album.title">
    <div class="card">
       <img :src="album.poster" alt="album.title">
       <h1>{{album.title}}</h1>
       <p>{{album.author}}</p>
       <p>{{album.year}}</p>
    </div>
   
  </div>
</div>
</template>

<script>
import axios from "axios";

export default {
 data(){
   return {
     albums: [],
     API_URL: "https://flynn.boolean.careers/exercises/api/array/music",
   }
 },
  mounted() {
    axios
    .get(this.API_URL)
    .then(r=>{
      this.albums = r.data.response;
    }).catch(e=>{
      console.log(e);
    })

  }
}
</script>

<style scoped lang="scss">

</style>
