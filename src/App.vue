<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  data() {
    return {
      counter1: 0,
      counter2: 0,
      timer1: "",
      timer2: "",
    };
  },
  components: {
    HelloWorld
  },
  mounted() {
    this.timer1 = setInterval(() => {
      this.counter1++;
    }, 1000);
    this.timer2 = setInterval(() => {
      this.counter2++;
    }, 1000);
  },
  methods: {
    stopTimer() {
      clearInterval(this.timer1);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
