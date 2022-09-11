<script lang="ts" setup>

</script>

<template>
    <div class="menu">
        <Logo />
    </div>
</template>
<style lang="postcss" scoped>
    .menu {
        height: 60px;
        @apply bg-gray-100;
        position: fixed;
        top: 0;
        z-index: 100;
        width:100%;
        @apply py-2;
        @apply flex items-center;
        @apply border-b-2;
        @apply border-gray-300;
    }

</style>
