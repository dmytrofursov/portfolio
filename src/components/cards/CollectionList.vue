<script setup>
import CollectionItem from './CollectionItem.vue';
import buildClient from '@datocms/cma-client-node';

const client = buildClient({
  apiToken: 'b5103d578b85fd73f1c2c8235b8d12',
});

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