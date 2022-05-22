<template>
    <div>
        <h2>Popup</h2>
        <input type="text" v-model="name" />
        <!-- $emit(eventname ,data which we want to pass to parent) -->
        <button @click="$emit('close', name)">Close Popup</button>
    </div>
</template>

<script>
export default {
    name: "Popup",
    // array of events that the componrt can emit to the parent component
    // we can give any name
    emits: {
        close: (name) => {
            if (!name) {
                return false;
            }
            return true;
        },
    },
    data() {
        return {
            name: "",
        };
    },
};
</script>
