<template>

    <div class="m-1 cards">
        <p>titolo: {{ListCardFilm.title}}</p> 
        <p>titolo originale: {{ListCardFilm.original_title}}</p>
        <p>lingua: {{ListCardFilm.original_language}}></p>
        <p>voto: {{ListCardFilm.vote_average}}</p>
    </div>

</template>
    
    
<script>

  export default {
  name: 'CardComp',
  props:{
    ListCardFilm: Object
   }
  }
</script>
    
    
<style lang="scss">
    .cards{
        border: 2px solid black;
    }

    .uk{
        width: 30px;
        height: 30px;
    }
</style>