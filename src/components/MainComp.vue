<template>

<div>

  <FilmList :List="List"/>
  
  <SerieList/>
  
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
      List: Array
    }
    
  }
</script>


<style lang="scss">

</style>