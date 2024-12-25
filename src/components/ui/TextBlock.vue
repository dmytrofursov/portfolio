<script setup>
const props = defineProps(["text"])
</script>

<template>
    <p class="text-block">
        {{ text }}
    </p>
</template>

<script>
export default {
    name: "TextBlock"
}
</script>

<style>
.text-block {
    color: #000000b3;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: 600;
}
</style>