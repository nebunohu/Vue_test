<template>
  <main>
    {{}}
    <CardComponent v-if="false" />
    <div class="playground">
      <CardComponent
        v-for="item in list"
        v-bind:key="item"
      />
    </div>
  </main>
</template>

<script>
import CardComponent from './components/CardComponent.vue';

export default {
  name: 'App',
  components: {
    CardComponent
  },
  data() {
    return {
      counter: 1,
      timerId: null,
      list: [1,2,3,4,5,6]
    }
  },
  mounted() {
    this.timerId = setInterval(() => {
      this.counter++;
    }, 1000)
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
