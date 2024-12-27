<script setup>
const props = defineProps([listItemClasses])
</script>

<template>
    <div role="listitem" class="CollectionItem {{listItemClasses}}">
            <slot></slot>
    </div>
</template>

<script>
export default {
    name: "Collection Item"
}
</script>

<style>
.CollectionItem {
    position: relative !important;
    padding-left: 10px !important;
    padding-right: 10px !important;
}

</style>