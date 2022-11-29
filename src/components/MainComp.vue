<template>

<div>
    <FilmList/>
   
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
  }
    
  }
</script>


<style lang="scss">

</style>