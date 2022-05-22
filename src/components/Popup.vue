<template>
    <div>
        <h2>Popup</h2>
        <!-- $emit(eventname ,data which we want to pass to parent) -->
        <button @click="$emit('close', 'omnish')">Close Popup</button>
    </div>
</template>

<script>
export default {
    name: "Popup",
    // array of events that the componrt can emit to the parent component
    // we can give any name
    emits: ["close"],
};
</script>
