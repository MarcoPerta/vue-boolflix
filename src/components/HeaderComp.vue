<template>
    <div class="d-flex justify-content-between align-items-center">
        <img src="../assets/netflix-logo-png-2582.png" alt="" class="netflix">
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


<style lang="scss" scoped>

 .netflix{
  width: 200px;
  height: 100px;
 }
 .searchbar{
  width: 400px;
 }
</style>