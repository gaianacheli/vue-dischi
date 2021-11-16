<template>
<div class="select_genre">
    <select class="select" name="type" id="type" v-model="filter" @change="$emit('filter-genre', filter)">
        <option value="">Scegli un genere</option>
        <option value="Pop">Pop</option>
        <option value="Metal">Metal</option>
        <option value="Jazz">Jazz</option>
        <option value="Rock">Rock</option>
    </select>
</div>
    
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
.select_genre {
    display: flex;
    justify-content: end;
    padding: 2rem;
    .select{
        background-color: rgba(46, 58, 70, 1);
        color: white;
        border-radius: 10px;
        padding: 10px;
    }
}

</style>