<script >
  export default{
    name:"App",
    data(){
      return{
          headingId:'heading',
          isDisabled: true
      }
    }
  }
</script>



<template>
    <h1 v-bind:id="headingId">id of this element is binding with v-bind:id</h1>

    <button v-bind:disabled="isDisabled">Hello</button>
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
