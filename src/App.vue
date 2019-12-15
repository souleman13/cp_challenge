<template>
  <div id="app" :class="{Border: ($mq === 'mobile+')}" >
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <ContentList :title='data.title' :content='data.content' />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ContentList from './components/ContentList.vue'
import data from './data/fakeContent.json'

export default {
  name: 'app',
  data(){
    return {data:data}
  },
  components: {
    // HelloWorld
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
.Border {
  /* border: 0 5vw; */
}
</style>
