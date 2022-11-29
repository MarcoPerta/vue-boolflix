<template>
 <div>
   <CardComp :List="List"/>
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