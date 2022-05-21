<script >
import Greet from "./components/Greet.vue";
export default {
    name: "App",
    data() {
        return {
            name: "lol",
        };
    },
    components: {
        Greet,
    },
};
</script>


<template>
    <Greet name="John" />
    <Greet name="Clerk" />
    <Greet name="Cena" />
    <Greet :name="name" />
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
