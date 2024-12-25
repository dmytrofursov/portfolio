<template>
    <section class="section">
        <slot></slot>     
    </section>
</template>
<script>
    export default {
        name: "Section"
    }
</script>
<style>
    .section {
        padding-top: 60px;
        padding-bottom: 60px;
    }
</style>