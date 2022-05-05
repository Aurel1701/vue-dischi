<template>
  <div id="app">
    <HeaderAlt/>
    <BoxCard :components="components" />
  </div>
</template>

<script>
import HeaderAlt  from './components/HeaderAlt.vue'

import BoxCard  from './components/BoxCard.vue'
import axios from 'axios';

export default {
  name: 'App',
  components: {
    HeaderAlt,
    
    BoxCard,
  },
  data(){
    return{
      components:[],

    };
    
  },
   mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
    console.log(response.data);
    this.components = response.data.response;
    })
  },
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
