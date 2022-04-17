<script >
export default {
  name: "App",
  data() {
    return {
      firstname: "Lol",
      lastname: "Arr",
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Leptop",
          price: 300,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      // call all time any  chages in ui
      console.log("getTotal from method called");
      return this.items.reduce((total, curr) => (total += curr.price), 0);
    },
  },
  computed: {
    fullname() {
      return `${this.firstname} ${this.lastname}`;
    },
    total() {
      // call only dependency is change
      console.log("total from computed called");
      return this.items.reduce((total, curr) => (total += curr.price), 0);
    },
  },
};
</script>



<template>
  <h1>Fullname - {{ firstname }} {{ lastname }}</h1>
  <h1>computed Fullname - {{ fullname }}</h1>

  <!-- advanrtages of computed properties -->
  <!-- if we need to use total many time then we need to write this logic many time -->
  <h2>Total - {{ items.reduce((total, curr) => (total += curr.price), 0) }}</h2>

  <button @click="items.push({ id: 4, title: 'keyboard', price: 50 })">
    Add Item
  </button>
  <!-- computed method both can be use in this case but computed have advantages of cache memory  -->
  <h2>Computed Total - {{ total }}</h2>
  <h2>Method Total - {{ getTotal() }}</h2>

  <input type="text" v-model="country" />
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
 