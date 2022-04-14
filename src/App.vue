<script >
  export default{
    name:"App",
    data(){
      return{
        greet:"hello",
        name:"abc",
        age:30
      }
    }
  }
</script>



<template>
  <h1>{{greet}}, {{name}}</h1>
  <div v-text="age"></div>

  <!-- gives error -->
  <!-- <div v-text="age">hello</div> -->
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
