<template>
<main class="main">
   <CardAlbum/>
</main>
 
</template>

<script>
import CardAlbum from './CardAlbum.vue';

export default {
  components:{
    CardAlbum,
  }
  }

</script>

<style scoped lang="scss">
@import '../assets/scss/variabili.scss';
main{
  background-color: $background_main;
  padding: 6rem 1rem;

}

</style>