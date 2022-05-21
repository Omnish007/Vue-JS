<script >
export default {
    name: "App",
    data() {
        return {
            volume: 0,
            movie: "Batman",
            movieInfo: {
                title: "",
                actor: "",
            },
            movieList: ["Batman", "superman"],
        };
    },
    methods: {},
    computed: {},
    watch: {
        volume(newValue, oldValue) {
            if (newValue > oldValue && newValue === 16) {
                alert(
                    "Listening to a high volume for a long time may damage your hearing"
                );
            }
        },

        // if we provide default value to movie property on page load api is not calling in console message
        // movie(newValue) {
        //     console.log(`calling api with movie name = ${newValue}`);
        // },

        // if we want to solve above problem then use below code
        movie: {
            handler(newValue) {
                console.log(`calling api with movie name = ${newValue}`);
            },
            // invoke function on page load
            immediate: true,
        },

        movieInfo: {
            handler(newValue) {
                console.log(
                    `calling api with movie title = ${newValue.title} and actor = ${newValue.actor}`
                );
            },
            // without deep : true watcher not track changes in object or array
            deep: true,
        },

        movieList: {
            handler(newValue) {
                console.log(`Update list ${newValue}`);
            },
            // deep: true,
        },
    },
};
</script>


<template>
    <h2>Volume Tracker (0-20)</h2>
    <h2>Current Volume {{ volume }}</h2>
    <div>
        <button @click="volume -= 2">-</button>
        <button @click="volume += 2">+</button>
    </div>
    <input type="text" v-model="movie" />

    <input type="text" v-model="movieInfo.title" />
    <input type="text" v-model="movieInfo.actor" />
    <!-- deep true is required since we mutet arr or obj  -->
    <!-- <button @click="movieList.push(['wonder women'])">Add movie - mutet</button> -->

    <!-- deep true is not required since we change refrence ofarr or obj  -->
    <button @click="movieList = movieList.concat(['wonder women'])">
        Add movie - new refrence
    </button>
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
