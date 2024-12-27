<script setup>
const props = defineProps([
    "sourceImg",
    "customAlt"
])
</script>

<template>
    <img sizes="(max-width: 479px) 100px, (max-width: 767px) 200px, (max-width: 1919px) 22vw, 370px" loading="eager"  alt={{customAlt}} src={{ sourceImg }} class="company-logo"/>
</template>

<script>
export default {
    name: "CompanyLogo"
}
</script>

<style>
.company-logo {
    width: 100% !important;
    object-fit: contain !important;
    overflow: clip !important; 
    aspect-ratio: 1 / 1 !important;
}
</style>