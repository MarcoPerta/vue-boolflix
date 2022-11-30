<template>

    <div class="cards-img m-1">
        <img :src="`https://image.tmdb.org/t/p/w185/${ListCardTv.poster_path}`" alt="" class="poster rounded">
        <div class="m-1 descriptions">
        <p>titolo: {{ListCardTv.name}}</p> <br>
        <p>titolo originale: {{ListCardTv.original_name}}</p>
        <span v-if="ListCardTv.original_language == 'en'">lingua: <img class="flag" src="../assets/flags/UK-union-flag.svg" alt=""></span>
        <span v-else-if="ListCardTv.original_language == 'it'"> lingua: <img class="flag" src="../assets/flags/italian-flag.svg" alt=""></span>
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

.flag{
    width: 30px;
    height: 25px;
}

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

.cards-img:hover .poster {
    opacity: 0.2;
}

</style>