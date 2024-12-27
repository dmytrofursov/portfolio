<script setup>
import CollectionItem from './CollectionItem.vue';

const props = defineProps([
    "sourceImg",
    "customAlt",
    "listItemClass"
])
</script>

<template>
    <CollectionItem listItemClasses={{ listItemClass }}>
        <img src={{ sourceImg }} class="company-logo"/>
    </CollectionItem>
</template>

<script>
export default {
    name: "CompanyLogo",
    components: {
        CollectionItem
    }
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