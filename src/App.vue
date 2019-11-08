<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <myFirst v-bind:dataTime="datatime"/>
    <examplecomputed />
    <fileMustacheSample/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import myFirst from './components/myFirst.vue';
import examplecomputed from './components/examplecomputed.vue';
import fileMustacheSample from './components/fileMustacheSample.vue';
export default {
  name: 'app',
  //注册cpn
  components: {
    HelloWorld,
    myFirst,
    examplecomputed,
    fileMustacheSample
  },
  data(){
    return {
      datatime :new Date
    }
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
  margin-top: 60px;
}
</style>
