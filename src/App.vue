<script >
export default {
  name: "App",
  data() {
    return {
      status: "danger",
      isPromoted: false,
      isSoldOut: true,
    };
  },
};
</script>



<template>
  <h1 class="underline">Underline text using static class</h1>
  <h1 v-bind:class="status">Change text color using dynamic class</h1>

  <!-- we can use binded class and static class also -->
  <h1 v-bind:class="status" class="underline">
    Use of static and dynamic class
  </h1>

  <!-- conditional binding  -->
  <h1 v-bind:class="isPromoted && 'promotede'">conditional binding</h1>

  <!-- ternary operators -->
  <h1 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Ternary operator</h1>

  <!-- binding with  array of classes -->
  <h1 v-bind:class="['sold-out', 'promoted']">Array of classes</h1>

  <!-- binding with  object of classes -->
  <h1
    v-bind:class="{
      'sold-out': isPromoted,
      new: isSoldOut,
    }"
  >
    Obj of classes
  </h1>
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

.underline {
  text-decoration: underline;
}

.danger {
  color: red;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>
