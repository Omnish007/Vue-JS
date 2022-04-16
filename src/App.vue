<script >
export default {
  name: "App",
  data() {
    return {
      base: 5,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    // don't accept arrow function in methods
    multiply(num) {
      // access data value using this keyword
      return num * this.base;
    },
  },
};
</script>



<template>
  <h1>{{ 2 + 7 + 1 + 17 }}</h1>
  <h1>Add method {{ add(2, 7, 18) }}</h1>
  <h1>Add method {{ multiply(9) }}</h1>
</template>

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
 