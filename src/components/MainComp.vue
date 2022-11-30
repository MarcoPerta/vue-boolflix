<template>

<div>

  <FilmList :List="List"/>
  
  <SerieList :ListTv="ListTv"/>
  
</div>

</template>


<script>
import FilmList from './FilmList.vue'
import SerieList from './SerieList.vue'

  export default {
    name: 'MainComp',
    components: {
    FilmList,
    SerieList
  },
  props:{
      List: Array,
      ListTv: Array
    }
    
  }
</script>


<style lang="scss" scoped>

</style>