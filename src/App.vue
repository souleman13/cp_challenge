<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <ContentList :title='data.title' :content='data.content' />
  </div>
</template>

<script>
import ContentList from './components/ContentList.vue'
import data from './data/fakeContent.json'

export default {
  name: 'app',
  data(){
    return {data:data}
  },
  components: {
    ContentList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
