<script lang="ts" setup>
import { MenuIcon } from '@vue-hero-icons/outline';
import { ref } from 'vue';

const open = ref(false);
</script>
<template>
    <div>
        <MenuIcon class="icon" @click="open = !open" :class="{'icon-opened': open}" />
    </div>
</template>
<style lang="postcss" scoped>
.icon {
    color: #CC99E9;
    width: 40px;
    height: 40px;
    @apply p-1;
    transition: all 0.2s;
}

.icon-opened {
    @apply text-gray-100;
    background-color: #CC99E9;
}
</style>
