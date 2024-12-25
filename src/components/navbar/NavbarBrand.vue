<template>
    <a href="/home" aria-current="page" aria-label="home" class="navbar-brand">
        <BrandLogo />
        <BrandName />
    </a>
</template>

<script>
import BrandLogo from "./BrandLogo.vue"
import BrandName from "./BrandName.vue"

export default {
    name: "NavbarBrand",
    components: {
        BrandLogo,
        BrandName
    }
}

</script>
<style>
.navbar-brand {
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    flex-flow: row;
    justify-content: center;
    align-items: center;
    min-width: 200px;
    margin-bottom: 0;
    margin-left: -5px;
    padding-top: 5px;
    padding-bottom: 5px;
    padding-left: 0;
    display: flex;
    float: left;
    color: #333 !important;
    text-decoration: none !important;
    position: relative;
    background-color: #0000;
;
}
</style>