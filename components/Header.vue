<script lang="ts" setup>
import Menu from './Menu.vue';

</script>

<template>
    <div class="header">
        <Logo />
        <Menu />
    </div>
</template>
<style lang="postcss" scoped>
    .header {
        @apply px-3;
        height: 60px;
        @apply bg-gray-100;
        position: fixed;
        top: 0;
        z-index: 100;
        width:100%;
        @apply py-2;
        @apply border-b-2;
        @apply border-gray-300;
        @apply flex items-center;
        @apply justify-between;

        @media screen(sm) {
            @apply justify-between;
        }
    }

</style>
