<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
  <!-- <NavBar/> -->
  <FirstArea/>
  <SecondArea/>
  <ThirdArea/>
  <FourthArea/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from './components/HelloWorld.vue';
import NavBar from './components/NavBar.vue';
import FirstArea from './components/FirstArea.vue'
import SecondArea from './components/SecondArea.vue'
import ThirdArea from './components/ThirdArea.vue'
import FourthArea from './components/FourthArea.vue';

@Options({
  components: {
    HelloWorld,
    NavBar,
    FirstArea,
    SecondArea,
    ThirdArea,
    FourthArea
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import "@/assets/scss/main.scss";

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  // color: #fff;
}
body {
  font-family: "Inter", sans-serif;
}
#app {
  font-family: "Inter",Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
