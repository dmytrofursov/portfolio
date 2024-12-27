<script setup>
import CollectionList from './CollectionList.vue'

const props = defineProps(["collectionListClass"])

</script>

<template>
    <div class="collection-list-wrapper">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: "CollectionListWrapper",
    components: {
        CollectionList
    }
}
</script>