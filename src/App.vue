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
    <Card>
        <template v-slot:header>
            <h3>Header</h3>
        </template>
        <template v-slot:default>
            <img src="https://picsum.photos/200" alt="" />
        </template>
        <template v-slot:footer>
            <button>vie details</button>
        </template>
    </Card>
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
