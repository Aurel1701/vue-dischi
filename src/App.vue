<template>
  <div id="app">
    <HeaderAlt/>
    <SearchBar :values="['All','Pop', 'Rock', 'Jazz', 'Metal']" @selectedGenere="filterResult"/>
    <BoxCard :components="components" />
  </div>
</template>

<script>
import HeaderAlt  from './components/HeaderAlt.vue'
import SearchBar  from './components/SearchBar .vue'
import BoxCard  from './components/BoxCard.vue'
import axios from 'axios';

export default {
  name: 'App',
  components: {
    HeaderAlt,
    BoxCard,
    SearchBar,
  },
  data(){
    return{
      components:[],
      filterGenere:[],

    };
    
  },
   mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
    console.log(response.data);
    this.components = response.data.response;
    this.filterGenere = response.data.response;
    })
  },
  methods: {
    filterResult(keyword){
      this.filterGenere = this.discs.filter((disc) => {
        return disc.genere.toLowerCase() === keyword.toLowerCase() || keyword.toLowerCase() === 'all';
      });
    }
  }
}
</script>

<style lang="scss">
#app {
  @import './style/common.scss';
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
