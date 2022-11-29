<template>
  <div id="app">

    <HeaderComp @emitSearchTextHeader="searchMovieAndTv"/>

    <MainComp :List="risultato" :ListTv="risultatoTv"/>

  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },
  data(){
    return{
      searchTextFromHeaderToApp: '',
      searchQueryUrl:'',
      risultato:[],
      searchQueryUrlTv:'',
      risultatoTv:[]
    }
  },
  mounted(){
  },
  methods:{
    searchMovieAndTv(searchTextHeader){
      this.searchTextFromHeaderToApp = searchTextHeader
      console.log(this.searchTextFromHeaderToApp)
      this.searchQueryUrl = 'https://api.themoviedb.org/3/search/movie?api_key=a46cf050fa06a3adc791073b9b0b4127&language=en-US&page=1&include_adult=false&query=' + this.searchTextFromHeaderToApp;
      this.searchQueryUrlTv = 'https://api.themoviedb.org/3/search/tv?api_key=a46cf050fa06a3adc791073b9b0b4127&language=en-US&page=1&include_adult=false&query=' + this.searchTextFromHeaderToApp;
      console.log(this.searchQueryUrl);
      console.log(this.searchQueryUrlTv);
      

      axios.get(this.searchQueryUrl)
      .then((response) => {
        this.risultato = response.data.results;
        this.risultatoTv = response.data.results
      })
    } 
  }
}


</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
