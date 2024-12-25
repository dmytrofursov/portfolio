<template>
    <div class="header" data-animation="default" data-collapse="medium" data-duration="400" data-easing="ease" data-easing2="ease" role="banner">
        <Container>
            <NavbarBrand />
            <NavMenu />
            <MenuButton />
        </Container>
    </div>
</template>

<script>
import Container from "../ui/Container.vue"
import NavMenu from './NavMenu.vue';
import NavbarBrand from "./NavbarBrand.vue";
import MenuButton from "./MenuButton.vue"

export default {
    name: "Header",
    components: {
        NavMenu,
        NavbarBrand,
        Container,
        MenuButton
    }
}
</script>

<style>
.header {
    position: relative ;
    background-color: #fff !important;
    background: #ddd;
    box-shadow: 0px 2px 75px #0000001a;
}

.header:before, .header:after {
    content: " ";
    grid-area: 1 / 1 / 2 / 2;
    display: table;
}

.header:after {
    clear: both;
}
</style>