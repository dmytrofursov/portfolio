<template>
    <div class="hero-camera">
        <div class="layout-grid hero-images"
            style="opacity: 1; transform: translate3d(0px, 0px, 0px) scale3d(1, 1, 1) rotateX(26deg) rotateY(0deg) rotateZ(9.5deg) skew(0deg, 0deg); transform-style: preserve-3d;">
            <img src="..\..\assets\images\cell-overview.png" class="hero-grid-image" loading="lazy" />
            <img src="..\..\assets\images\cell-overview.png" class="hero-grid-image" loading="lazy" />
            <img src="..\..\assets\images\cell-overview.png" class="hero-grid-image" loading="lazy" />
            <img src="..\..\assets\images\cell-overview.png" class="hero-grid-image-bottom" loading="lazy" />
            <img src="..\..\assets\images\cell-overview.png" class="hero-grid-image-bottom" loading="lazy" />
            <img src="..\..\assets\images\cell-overview.png" class="hero-grid-image-bottom" loading="lazy" />
        </div>
    </div>
</template>

<script>
export default {
    name: "HeroCamera",
    components: {

    }
}
</script>

<style>
.hero-camera {
    box-sizing: content-box;
    perspective: 1000px;
    height: 35vw;
    overflow: hidden;
    transform: translate(0);
}

.hero-images {
    grid-column-gap: 3vw;
    grid-row-gap: 3vw;
    grid-template-columns: 1fr 1fr 1fr;
}

.hero-grid-image {
    aspect-ratio: 16 / 9;
    object-fit: cover;
    width: 100%;
    max-width: 100%;
    animation: adjust-position linear forwards;
    animation-timeline: scroll(root block);
    animation-duration: 4s !important;
}

.hero-grid-image-bottom {
    flex-direction: row-reverse;
    animation: adjust-position-reverse linear forwards !important;
    animation-timeline: scroll(root block) !important;
    animation-duration: 4s !important;
}

@keyframes adjust-position {

    /* Start position: shift entire column up, but not so that it goes out of view */
    from {
        transform: translateX(calc(-100% + 100vh));
    }

    /* End position: shift entire column down, but not so that it goes out of view */
    to {
        transform: translateX(calc(100% - 100vh));
    }
}

@keyframes adjust-position-reverse {

/* Start position: shift entire column up, but not so that it goes out of view */
from {
    transform: translateX(calc(100% - 100vh));
}

/* End position: shift entire column down, but not so that it goes out of view */
to {
    transform: translateX(calc(-100% + 100vh));
}
}
</style>