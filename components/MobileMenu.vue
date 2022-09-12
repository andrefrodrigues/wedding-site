<script lang="ts" setup>
import { MenuIcon } from '@vue-hero-icons/outline';
import { ref } from 'vue';

type MenuItem = {
    name: string;
    id: string;
};

type Props = {
    menuItems: MenuItem[];
}

const { menuItems } = defineProps<Props>();
const open = ref(false);


</script>
<template>
    <div>
        <MenuIcon class="icon" @click="open = !open" :class="{'icon-opened': open}" tabindex="0" />
            <transition-group v-if="open" name="menu" tag="ul" class="menu">
                <li v-for="item in menuItems" :key="item.id" @click="open = !open">
                    <Anchor  :id="item.id" class="menu-item">
                        {{item.name}}
                    </Anchor>
                </li>
            </transition-group>
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

.menu {
    @apply fixed;
    right: 0;
    top: 58px;
    width:100%;
}

.menu-item {
    @apply inline-block;
    @apply bg-gray-100;
    color: #CC99E9;
    font-weight: 600;
    width: 100%;
    @apply p-3;
    outline: none;
}

.menu-item:hover, .menu-item:focus, .menu-item:active {
    @apply text-gray-100 bg-indigo-200;
}


.menu-enter-active, .menu-leave-active {
  transition: all 10s;
}
.menu-enter, .menu-leave-to /* .list-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(30px);
}
</style>
