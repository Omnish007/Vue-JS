<script >
import ComponentC from "./components/ComponentC.vue";

export default {
    name: "App",
    data() {
        return {
            name: "Omnish",
        };
    },
    provide() {
        return {
            username: this.name,
        };
    },
    components: {
        ComponentC,
    },
};
</script>


<template>
    <!-- we cannot use username in component from we provide the value  -->
    <!-- for Ex. we provide user-name from App compo so we can not directly use in
    app we need to add in data propertie -->
    <h2>App component - Username:{{ name }}</h2>
    <ComponentC />
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
