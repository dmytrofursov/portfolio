<script setup>
const proprs = defineProps(["linkText", "linkSource", "target"])
</script>

<template>
    <a style="max-width: 1200px;" target="{{ target }}" class="nav-link" href={{linkSource}}>
        {{ linkText }}
    </a>
</template>

<script>

export default {
    name: "NavLink",
}
</script>

<style>
.nav-link {
    vertical-align: top;
    color: #222 !important;
    text-align: left;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
    text-decoration: none !important;
    display: inline-block;
    position: relative;
    font-weight: 400;
}
</style>