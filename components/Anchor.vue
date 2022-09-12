<script setup lang="ts">

    type Props = {
        id: string;
    }

    const { id } = defineProps<Props>();

    const onAnchorClick = () => {
        document.getElementById(id)?.scrollIntoView();
    };
</script>
<template>
    <span class="anchor" @click="onAnchorClick">
        <slot />
    </span>
</template>
<style lang="postcss" scoped>
    .anchor {
        cursor: pointer;
    }
</style>
