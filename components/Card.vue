<script lang="ts" setup>
type Props = {
    title: string;
    image: string;
}

const { title, image } = defineProps<Props>();

</script>


<template>
    <div class="card">
        <h2 class="card-title">{{title}}</h2>
        <img class="card-img" :src="image">
    </div>
</template>

<style lang="postcss" scoped>
.card {
    @apply mt-12;
    @apply relative;
    transition: all 500ms;
    width: 100%;

    @media screen(sm) {
        width: 450px;
        height: 300px;
        @apply mt-0;
    }
}

.card:hover {
    transform: scale(1.2);
}

.card:hover>.card-img {
    filter: none;
}

.card:hover>.card-title {
    @apply bg-indigo-200;
}

.card-title {
    @apply text-center;
    transition: background-color 500ms;
    @apply w-full;
    @apply text-3xl;
    @apply absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2;
    z-index: 1;
}

.card-img {
    filter: brightness(50%);
    @media screen(sm) {
        width: 450px;
        height: 300px;
    }
}
</style>
