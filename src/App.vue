<template>
  <main>
    <!--{{this.charactersList}}
    <CardComponent v-if="false" />
    <div class="playground">
      <CardComponent
        v-for="item in list"
        v-bind:key="item"
      />
    </div>-->
    <CharacterCard :charactersList="charactersList" />
  </main>
</template>

<script>
import CardComponent from './components/CardComponent.vue';
import CharacterCard from './components/CharacterCard.vue';
// Consts
import { API_BASE_URL, CHARACTER } from "./consts/consts.js";

export default {
  name: 'App',
  components: {
    CardComponent,
    CharacterCard
  },
  data() {
    return {
      list: [1,2,3,4,5,6],
      charactersList: [{name: ''}]
    }
  },
  beforMounted() {
    /*const getCharactersList = async () => {
      const res = await fetch(API_BASE_URL+CHARACTER);
      const data = await res.json();
      this.charactersList = data.results;
    };
    getCharactersList();*/
  },
  methods: {
    stopCounter: function() {
      clearInterval(this.timerId);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  background-color: #cfd0cf;
  width: 100%;
  height: 100%;
}

.playground {
  width: 390px;
  display: flex;
  flex-flow: row wrap;
}

html {
  height: 100%;
}

body {
  margin: 0;
  height: 100%;
}
</style>
