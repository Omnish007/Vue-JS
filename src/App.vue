<script >
export default {
  name: "App",
  data() {
    return {
      names: ["Lol", "Arr", "Foo"],
      fullNames: [
        { first: "Lol", last: "last lol" },
        { first: "Arr", last: "last Arr" },
        { first: "foo", last: "last foo" },
      ],
      actors: [
        {
          name: "lol",
          movies: ["lol1", "lol2"],
        },
        {
          name: "Arr",
          movies: ["Arr1", "Arr2"],
        },
        {
          name: "foo",
          movies: ["foo1", "foo2"],
        },
      ],

      myinfo: {
        name: "Arr",
        age: "Foo",
      },
    };
  },
};
</script>



<template>
  <!-- iterate using array  -->
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <hr />

  <!-- iterate using array of object  -->
  <h2 v-for="(name, index) in fullNames" :key="index">
    {{ index }} {{ name.first }} - {{ name.last }}
  </h2>
  <hr />

  <!-- iterate using array of array  -->
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <span v-for="movie in actor.movies" :key="movie">{{ movie }}</span>
  </div>
  <hr />

  <!-- iterate using object  -->
  <h2 v-for="(value, key, index) in myinfo" :key="index">
    {{ value }} - {{ key }} - {{ index }}
  </h2>
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
