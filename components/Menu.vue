<script setup lang="ts">
import { computed } from 'vue';


const menuData = [
    {name: 'Inicio', id: 'hero'},
    { name: 'Cerimónia', id: 'ceremony' },
    { name: 'Festa', id: 'party' },
    { name: 'Onde ficar', id: 'accomodation' },
    {name: 'Curiosidades', id: 'curiosities'},
]

const menuItems = computed(() => menuData);
</script>
<template>
    <div class="menu-wrapper">
        <MobileMenu class="mobile-menu" :menu-items="menuItems" />
        <ul class="menu">
            <li v-for="item in menuItems" :key="item.id">
                <Anchor :id="item.id" class="menu-item">
                    {{item.name}}
                </Anchor>
            </li>
        </ul>
    </div>
</template>
<style lang="postcss" scoped>
.mobile-menu {
    @media screen(sm) {
        @apply hidden;
    }
}

.menu-wrapper {

    @media screen(sm) {
        @apply flex-1;

    }
}

.menu {
    @apply hidden;

    @media screen(sm) {
        @apply flex items-center justify-center;
    }
}

.menu-item {
    @apply text-lg;
    color: #CC99E9;
    font-weight: 600;
    @apply mr-10;
}

.menu-item:hover {
    @apply text-indigo-200;
    transition: color 0.3s ease;
}


</style>
