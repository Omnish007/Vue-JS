<script >
import Card from "./components/Card.vue";

export default {
    name: "App",
    data() {
        return {};
    },
    components: {
        Card,
    },
    methods: {},
};
</script>


<template>
    <!-- pass any content and in child component slot tag is replace by the content 
    between custom component tag -->
    <Card></Card>
    <Card>Card Content</Card>
    <Card><h2>Card Content</h2></Card>
    <Card><img src="https://picsum.photos/200" /> </Card>
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
