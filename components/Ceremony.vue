<script lang="ts" setup>
import { ref } from 'vue';

const isPortrait = ref(window.screen.orientation.type === 'portrait-primary');

const handleOrientationChange = () => {
    isPortrait.value = window.screen.orientation.type === 'portrait-primary';
};

window.addEventListener('orientationchange', handleOrientationChange);
</script>
<template>
    <section class="ceremony" id="ceremony" :class="{'viewport-height': isPortrait}">
        <div class="content">
            <Anchor id="ceremony">
                <h1 class="title"><img class="rings" src="rings.png">Cerimónia</h1>
            </Anchor>
            <div class="card-wrapper">
                <a href="https://se-braga.pt/" target="_blank">
                    <Card title="Sé de Braga" image="se-braga.jpeg" />
                </a>
                <a href="https://maps.google.pt/maps?q=S%C3%A9%20Catedral%20de%20braga&t=&z=17&ie=UTF8&iwloc="
                    target="_blank">
                    <Card title="Localização" image="mapa-se.png" />
                </a>
            </div>
        </div>
    </section>
</template>
<style lang="postcss" scoped>
.card-wrapper {
    @apply flex flex-col justify-around;

    @media screen(sm) {
        @apply w-full;
        @apply mt-64;
        @apply flex-row;
    }
}

.content {
    @apply relative;
    z-index: 1;
}

.viewport-height {
    height: 100vh;
    min-height: 500px;
}

.ceremony {
    scroll-margin-top: 60px;
    @apply p-9;
    @apply text-center;
    @apply relative;
    @apply bg-indigo-200;

    @media screen(md) {
        height: 100vh;
    }
}

.ceremony::after {
    content: "";
    display: block;
    position: absolute;
    height: 100%;
    width: 100%;
    background-image: url('https://images.unsplash.com/photo-1524650448000-02d0a2aeb6cb?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    top: 0;
    opacity: 0.6;
    @apply -mx-9;
}

.title {
    @apply text-5xl;
    @apply flex items-center justify-center;

    @media screen(md) {
        @apply text-6xl;
    }
}

.time {
    @apply text-4xl;
    @apply mb-12;

    @media screen(md) {
        @apply mb-24;
    }
}

.rings {
    display: inline;
    width: 48px;
    height: 48px;
    @apply mr-2;
}
</style>
