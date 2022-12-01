<template>
 <div class="d-flex justify-content-between scroll">
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
 .scroll{
  overflow-x: auto;
  overflow-y: hidden;
}
</style>