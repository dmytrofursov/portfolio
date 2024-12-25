<script setup>
const {headingText = "Heading"} = defineProps(["headingText"])
</script>

<template>
    <h1 class="heading">
        {{ headingText }}
    </h1>
</template>

<script>
export default {
    name: "Heading"
}
</script>

<style>
.heading {
    max-width: 450px;
    margin-bottom: 30px;
    font-family: Poppins, sans-serif;
    font-weight: 400;
}
</style>