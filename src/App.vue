<script>
import AppFilter from './components/AppFilter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import axios from 'axios'

import {store} from './store';


export default {

  data(){
    
    return {
      store,
    }

  },
  
  components: {
    AppHeader,
    AppFilter,
    AppMain,
  },

  created(){
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then(response =>  (this.store.CharacterList = response.data.data));
  }

}
</script>

<template>
  <AppHeader/>
  <AppFilter/>
  <AppMain/> 
</template>

<style lang="scss" scoped>
@use "./assets/style/general.scss"


</style>


