<template>

    <div class="m-1 cards">
        <p>titolo: {{ListCardTv.original_title}}</p> 
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
    
    
<style lang="scss">
    .cards{
        border: 2px solid black;
    }

</style>