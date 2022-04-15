<script >
export default {
  name: "App",
  data() {
    return {
      highlight: "purple",
      headerStyles: {
        color: "orange",
        fontSize: "30px",
        textDecoration: "underline",
      },
      bgStyle: {
        "background-color": "red",
      },
    };
  },
};
</script>



<template>
  <!-- it also allows camel case in styles like "font-size" and fontSize -->
  <h1 v-bind:style="{ color: highlight, fontSize: '50px' }">Initial styles</h1>

  <!-- pass classes object -->
  <h1 v-bind:style="headerStyles">Initial styles</h1>

  <!-- pass classes array -->
  <h1 v-bind:style="[headerStyles, bgStyle]">Initial styles</h1>
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
