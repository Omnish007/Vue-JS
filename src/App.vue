<script >
export default {
  name: "App",
  data() {
    return {
      num: "27",
      display: true,
      showElement: true,
    };
  },
};
</script>



<template>
  <!-- v-if  -->
  <h1 v-if="num === 0">Number is 0</h1>
  <h1 v-if="num === 5">Number is 5</h1>
  <hr />

  <!-- v-else -->
  <h1 v-if="num === 5">Number is 5</h1>
  <h2 v-else>Number is not equal to 5</h2>
  <hr />

  <!-- v-else-if -->
  <h1 v-if="num === 0">Number is 0</h1>
  <h2 v-else-if="num < 0">Number is negative</h2>
  <h2 v-else-if="num > 0">Number is positive</h2>
  <h2 v-else>Not a number</h2>

  <!-- we can pass div also but div is rendered in dom template is not -->
  <template v-if="display">
    <h1>Vue</h1>
    <h1>Js</h1>
    <h1>Front-end</h1>
  </template>

  <!-- diffrence between v-if and v-show if it return false then v-if element is not present in dom but v-show element is present in dom with display none propertie -->
  <!-- v-show -->
  <h2 v-show="showElement">Using v-show</h2>
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
