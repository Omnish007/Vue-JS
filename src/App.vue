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
    changeName(event) {
      this.name = "LoL";
      console.log(event);
    },
    increment(num, event) {
      console.log(event);
      this.count += num;
    },
    decrement(num) {
      this.count -= num;
    },
  },
};
</script>



<template>
  <!-- we can replace v-on: to @ -->

  <h1>{{ name }}</h1>
  <div>
    <button @click="changeName">Change name</button>
  </div>
  <hr />

  <div>
    <h1>{{ count }}</h1>
    <button @click="increment(5, $event)">Increment</button>
    <button @click="decrement(2)">Decrement</button>
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
 