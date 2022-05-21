<script >
export default {
    name: "App",
    data() {
        return {
            firstname: "Lol",
            lastname: "Arr",
        };
    },
    methods: {
        getTotal() {
            // call all time any  chages in ui
            console.log("getTotal from method called");
            return this.items.reduce((total, curr) => (total += curr.price), 0);
        },

        changeFullName() {
            this.fullname = "Clark Kent";
        },
    },
    computed: {
        fullname: {
            get() {
                return `${this.firstname} ${this.lastname}`;
            },
            set(value) {
                const names = value.split(" ");
                this.firstname = names[0];
                this.lastname = names[1];
            },
        },
    },
};
</script>


<template>
    <h1>Fullname - {{ firstname }} {{ lastname }}</h1>
    <h1>computed Fullname - {{ fullname }}</h1>

    <button @click="changeFullName">Changr fullname</button>
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
