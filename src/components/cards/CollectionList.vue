<script setup>
import CollectionItem from './CollectionItem.vue';

const props = defineProps(["listClass"])
</script>

<template>
    <div role="list" class={{ listClass }}>
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: "CollectionList",
    components: {
        CollectionItem
    }
}
</script>   