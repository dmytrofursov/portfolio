<template>
    <div class="container">
        <slot></slot>
    </div>
</template>
<script>
export default {
    name: "Container"
}
</script>
<style>
.container {
    text-align: left;
    max-width: 1200px;
    padding-left: 30px;
    padding-right: 30px;
    display: block;
    margin-left: auto;
    margin-right: auto;
}
</style>