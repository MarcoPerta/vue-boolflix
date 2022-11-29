<template>
 <div class="d-flex flex-wrap justify-content-between">
   <CardComp v-for="(elem,index) in List" :key="index" :ListCardFilm="elem"/>
 </div>
</template>
 
 
<script>
import CardComp from './CardComp.vue'

   export default {
    name: 'FilmList',
    components: {
      CardComp
   },
   props:{
      List: Array
   }
    
   }
</script>
 
 
<style lang="scss">
 
</style>