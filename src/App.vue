<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
  <NavBar/>
  <FirstArea/>
  <SecondArea/>
  <ThirdArea/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from './components/HelloWorld.vue';
import NavBar from './components/NavBar.vue';
import FirstArea from './components/FirstArea.vue'
import SecondArea from './components/SecondArea.vue'
import ThirdArea from './components/ThirdArea.vue'

@Options({
  components: {
    HelloWorld,
    NavBar,
    FirstArea,
    SecondArea,
    ThirdArea
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
a, a:link, a:hover, a:active, a:focus, a:visited {
  text-decoration: none;

}
body {
  font-family: "Inter", sans-serif;
}
#app {
  font-family: "Inter",Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000;
}
</style>
