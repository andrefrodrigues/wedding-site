<script lang="ts" setup>

</script>
<template>
    <section class="curiosities" id="curiosities">
        <div class="content">
            <Anchor id="curiosities">
                <h1 class="title">Curiosidades</h1>
            </Anchor>
        </div>
    </section>
</template>
<style lang="postcss" scoped>
.curiosities {
    scroll-margin-top: 60px;
    @apply text-center;
    @apply p-9;
    height: 100vh;
    @apply bg-indigo-300;
    @apply relative;
}

.content {
    @apply relative;
    z-index: 1;
}

.title {
    @apply text-5xl;
    @apply flex items-center justify-center;

    @media screen(md) {
        @apply text-6xl;
    }
}
</style>
