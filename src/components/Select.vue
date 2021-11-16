<template>
    <select class="select" name="type" id="type" v-model="filter" @change="$emit('filter-genre', filter)">
        <option value="">Scegli un genere</option>
        <option value="Pop">Pop</option>
        <option value="Metal">Metal</option>
        <option value="Jazz">Jazz</option>
        <option value="Rock">Rock</option>
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