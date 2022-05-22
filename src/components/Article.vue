<template>
    <h2>Article</h2>
    <h2>Title: {{ title }}</h2>
    <h2>Likes: {{ likes }}</h2>
    <h2>Published: {{ isPublished }}</h2>
</template>

<script>
export default {
    name: "Article",
    props: {
        title: {
            type: String,
            required: true,
            default: "Default Title",
        },
        likes: Number,
        isPublished: Boolean,
    },
};
</script>
