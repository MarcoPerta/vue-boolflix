<template>
 <div class="d-flex scroll justify-content-between">
  <CardCompTv v-for="(elem,index) in ListTv" :key="index" :ListCardTv="elem"/>
 </div>
</template>
 
 
<script>
 import CardCompTv from './CardCompTv.vue'

   export default {
    name: 'SerieList',
    components: {
      CardCompTv
   },
    props:{
      ListTv: Array
    }

   }
</script>
 
 
<style lang="scss">
 .scroll{
  overflow-x: auto;
  overflow-y: hidden;
}
</style>