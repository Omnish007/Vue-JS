<script >
export default {
  name: "App",
  data() {
    return {
      names: ["Lol", "Arr", "Foo"],
    };
  },
};
</script>



<template>
  <!-- conditional list rendering  -->
  <template v-for="name in names" :key="name">
    <h1 v-if="name === 'Lol'">{{ name }}</h1>
  </template>
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
 