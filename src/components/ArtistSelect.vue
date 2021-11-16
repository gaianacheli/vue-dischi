<template>
    <select class="select" name="type" id="type" v-model="filter" @change="$emit('filter-artist', filter)">
        <option value="">Scegli un artista</option>
        <option value="Bon Jovi">Bon Jovi</option>
        <option value="Queen">Queen</option>
        <option value="String">String</option>
        <option value="Steve Gadd Band">Steve Gadd Band</option>
        <option value="Iron Maiden">Iron Maiden</option>
        <option value="Micheal Jacjson">Micheal Jacjson</option>
        <option value="Dave Weckl">Dave Weckl</option>
        <option value="Metallica">Metallica</option>
        <option value="Deep Purple">Deep Purple</option>
        <option value="Eric Clapton">Iron Maiden</option>
    </select>
    
</template>


<script>
export default {
  data() {
    return {
      filter: "",
    };
  },
};
</script>


<style scoped lang="scss">
   @import "../assets/scss/common.scss";

</style>
