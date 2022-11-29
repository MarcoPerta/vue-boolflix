<template>
    <div>
        <div class="searchbar">
            <input type="text" class="form-control" v-model="searchText" @keyup.enter="$emit('emitSearchTextHeader', searchText)">
            <!-- <button class="btn btn-primary">Submit</button> -->
        </div>
    </div>
</template>
 

<script>

  export default {
    name: 'HeaderComp',

    data(){
    return{
      searchText: ''
    }
  }
  }
  
</script>


<style lang="scss">

</style>