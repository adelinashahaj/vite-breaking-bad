<template>

  <MyHeader title="YU-GI-OH Api"/>

  <main>
    <AppSelect @doSelect="getCards" />

    <ResultMessage/>
  <CharactersList/>
  </main>

</template>

<script>
import axios from 'axios';
import { store } from './store.js';
import MyHeader from './components/MyHeader.vue';
import AppSelect from './components/AppSelect.vue';
import CharactersList from './components/CharactersList.vue';
import ResultMessage from './components/ResultMessage.vue';


export default {

  components: {
    MyHeader,
    CharactersList,
    AppSelect,
    ResultMessage
  },
  data(){
    return {
      store
    }

  },
  methods: {
    getCards() {

      let urlApi = 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=30&offset=0';
     
        if (store.select.length > 0) {
          urlApi += `?&archetype=${store.select}`;
        }

    axios.get(urlApi)
    .then(response => {
      this.store.charactersList = response.data.data;
      console.log(this.store.charactersList);
     
    })
  }
 
  },
   created() {
    this.getCards();
  }


}

</script>


<style lang="scss">
 @use './styles/general.scss'

</style>
