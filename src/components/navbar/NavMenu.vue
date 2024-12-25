<template>
    <nav role="navigation" class="nav-menu">
        <NavLink target="_blank" linkText="Resume" linkSource="/resume" />
        <NavLink class="button" linkText="Say hi!" linkSource="#email-form" />
    </nav>
</template>

<script>
import NavLink from "../navbar/NavLink.vue"
export default {
    name: "NavMenu",
    components: {
        NavLink
    }
}
</script>
<style>
.nav-menu {
    unicode-bidi: isolate;
    position: relative;
    float: right;
}

.nav-link.button {
    background-color: var(--main-brand-color);
    color: #fff !important;
    border-radius: 6px;
    margin-top: 12px;
    padding-top: 8px;
    padding-bottom: 8px;
    font-weight: 400;
}
</style>