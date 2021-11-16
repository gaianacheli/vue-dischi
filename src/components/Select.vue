<template>
<div class="select_genre">
    <select name="type" id="type" v-model="filter" @change="$emit('filter-genre', filter)">
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