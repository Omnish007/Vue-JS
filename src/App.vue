<script >
  export default{
    name:"App",
    data(){
      return{
        greet:"hello",
        name:"abc",
        age:"<b>30</b>",
        hack:`<a href='#' onClick="alert('you have been hacked !')"> Win a prize!</a>`
      }
    }
  }
</script>



<template>

  <!-- both render as plain text  -->
  <div>{{age}}</div>
  <div v-text="age"></div>

  <!-- rendered as html  -->
  <div v-html="age"></div>

  <!-- don't use other non trusted api data as v-html because it can cause cross-site scripting attack -->
  <!-- ex....  -->
  <div  v-html="hack"></div>

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
