<template>
  <div id="app">
      <p class="red">{{ saluto }}</p>
      <div v-for="(item, index) in test" :key="index">
          {{ item }}
        <AppTitleComponent/>
      </div>
  </div>
</template>

<script>
import AppTitleComponent from './components/AppTitleComponent.vue'

export default {
  name: 'App',
  components: {
    AppTitleComponent
   
  },
  data() {
    return {
      saluto: 'Hello World!',
      test: [1, 2, 4, 8, 16, 32],
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
