<template>
    <!-- if we have root  element in component and we pass id from perent component (in this ex app is parent) id="my-article" then this is is apply on parent element of this component -->
    <!-- if we do not have root element then if from parent is not apply to any component -->

    <div>
        <h2>Article</h2>
        <!-- if we want to add id to below, if we have root element then id apply on both , if we don not want to add id to both then we need to pass option in export -> inheritAttrs: false -->
        <h2 v-bind="$attrs">Title: {{ title }}</h2>
        <h2>Likes: {{ likes }}</h2>
        <h2>Published: {{ isPublished }}</h2>
    </div>
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
    // if we don not want to add id to both then we need to pass option in export -> inheritAttrs: false
    inheritAttrs: false,
};
</script>
