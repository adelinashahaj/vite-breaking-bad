<template>

  <MyHeader title="YU-GI-OH Api"/>

  <main>
    <AppSearch />
  <CharactersList/>
  </main>

</template>

<script>
import axios from 'axios';
import { store } from './store.js';
import MyHeader from './components/MyHeader.vue';
import AppSearch from './components/AppSearch.vue';
import CharactersList from './components/CharactersList.vue';


export default {

  components: {
    MyHeader,
    CharactersList,
    AppSearch
  },
  data(){
    return {
      store
    }

  },
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=Blue-Eyes')
    .then(response => {
      this.store.charactersList = response.data.data;
     
    })

  }


}

</script>


<style lang="scss">
 @use './styles/general.scss'

</style>
