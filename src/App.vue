<script setup>
import { ref } from "vue";
import Input from "./components/Input.vue";
const name = ref("");
</script>

<template>
    {{ name }}
    <Input v-model="name" />
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
