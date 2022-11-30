<template>

    <div class="cards-img m-1">
        <img :src="`https://image.tmdb.org/t/p/w185/${ListCardTv.poster_path}`" alt="" class="rounded">
        <div class="m-1 descriptions">
        <p>titolo: {{ListCardTv.name}}</p> 
        <p>titolo originale: {{ListCardTv.original_name}}</p>
        <p>lingua: {{ListCardTv.original_language}}</p>
        <p>voto: {{ListCardTv.vote_average}}</p>
        </div>
    </div>

</template>
    
    
<script>

  export default {
  name: 'CardCompTv',
  props:{
    ListCardTv: Object
   }
  }
</script>
    
    
<style lang="scss" scoped>

.cards-img {
    position: relative;
}

.descriptions {
    border: 2px solid black;
    display: none;
    width: 100%;
}

.cards-img:hover .descriptions {
    display: block;
    position: absolute;
    top: 0;
    left: 0;
}

.cards-img:hover img {
    opacity: 0.2;
}

</style>