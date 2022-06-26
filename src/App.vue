<script >
import NameList from "./components/NameList.vue";

export default {
    name: "App",
    data() {
        return {};
    },
    components: {
        NameList,
    },
    methods: {},
};
</script>


<template>
    <NameList>
        <template v-slot:default="slotProps">
            {{ slotProps.firstName }} {{ slotProps.lastName }}
        </template>
    </NameList>
    <NameList>
        <template v-slot:default="slotProps">
            {{ slotProps.lastName }} {{ slotProps.firstName }}
        </template>
    </NameList>
    <NameList>
        <template v-slot:default="slotProps">
            {{ slotProps.firstName }}
        </template>
    </NameList>
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
