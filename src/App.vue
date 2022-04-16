<script >
export default {
  name: "App",
  data() {
    return {
      name: "Arr",
      count: 0,
    };
  },
  methods: {
    increment(num) {
      this.count += num;
    },
    decrement(num) {
      this.count -= num;
    },
  },
};
</script>

<template>
  <h1>{{ name }}</h1>
  <div>
    <button v-on:click="name = 'Lol'">Change name</button>
  </div>
  <hr />

  <div>
    <h1>{{ count }}</h1>
    <button v-on:click="increment(5)">Increment</button>
    <button v-on:click="decrement(2)">Decrement</button>
  </div>
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
 