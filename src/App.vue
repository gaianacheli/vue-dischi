<template>
  <div id="app">
  <SiteHeader/>
  <SiteMain/>
  <SiteFooter/>

  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue';
import SiteMain from './components/SiteMain.vue';
import SiteFooter from './components/SiteFooter.vue';



export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter
    
   
  }
}
</script>

<style lang="scss">
@import '../src/assets/scss/variabili.scss';
@import "../node_modules/bootstrap/scss/bootstrap.scss";

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
