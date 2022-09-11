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
        <a href="#ceremony">
            <h1 class="title"><img class="rings" src="rings.png">Cerimónia</h1>
        </a>
        <h1 class="church">Sé de Braga</h1>
        <h2 class="time">11h15</h2>
        <ChurchMap />
    </section>
</template>
<style lang="postcss" scoped>

.viewport-height {
    height: calc(100vh - 60px);
    min-height: 500px;
}
.ceremony {
    @apply p-10;
    @apply text-center;
    @apply relative;
    @apply bg-indigo-200;

    @media screen(md) {
        height: calc(100vh - 60px);
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
    @apply -mx-10;
}

.title {
    @apply relative;
    z-index: 1;
    @apply text-5xl;
    @apply flex items-center justify-center;

    @media screen(md) {
        @apply text-6xl;
    }
}

.church {
    @apply relative;
    z-index: 1;
    @apply text-4xl;
    @apply mt-10;

}

.time {
    @apply relative;
    z-index: 1;
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
