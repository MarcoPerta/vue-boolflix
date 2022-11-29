<template>
 <div class="d-flex flex-wrap justify-content-between">
    <div v-for="(elem,index) in List" :key="index" class="m-1 cards">
        <p>titolo: {{elem.title}}</p> 
        <p>titolo originale: {{elem.original_title}}</p>
        <p>lingua: {{elem.original_language}}</p>
        <p>voto: {{elem.vote_average}}</p>
    </div>
 </div>
</template>
    
    
<script>

  export default {
  name: 'CardComp',
  props:{
      List: Array
   }
  }
</script>
    
    
<style lang="scss">
    .cards{
        border: 2px solid black;
    }
</style>