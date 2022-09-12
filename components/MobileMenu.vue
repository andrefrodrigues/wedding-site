<script lang="ts" setup>
import { MenuIcon } from '@vue-hero-icons/outline';
import { ref } from 'vue';

const open = ref(false);

const onFocusOut = () => {
    open.value = false;
};
</script>
<template>
    <div>
        <MenuIcon class="icon" @click="open = !open" :class="{'icon-opened': open}" tabindex="0" @focusout="onFocusOut"/>
    </div>
</template>
<style lang="postcss" scoped>
.icon {
    color: #CC99E9;
    width: 40px;
    height: 40px;
    @apply p-1;
    transition: all 0.2s;
    outline: none;
}

.icon-opened {
    @apply text-gray-100;
    background-color: #CC99E9;
}
</style>
