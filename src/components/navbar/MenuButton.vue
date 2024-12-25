<template>
    <div class="menu-button" aria-label="menu" role="button" tabindex="0" aria-controls="nav-overlay-0"
        aria-haspopup="menu" aria-expanded="false">
        <img src="../../assets/images/navigation.png" alt="menu button">
    </div>
</template>

<script>
export default {
    name: "MenuButton"
}
</script>

<style>
.menu-button {
    float: right;
    cursor: pointer;
    position: relative;
    width: 25px;
    display: none;
    height:auto
}

.menu-button:focus {
    outline: 0;
}
</style>