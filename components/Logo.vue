<template>
    <span class="logo">
        <img src="lavender.png"/>
        <span class="names">Elisa & André</span>
    </span>
</template>

<style lang="postcss" scoped>
    .logo {
        @apply flex items-center;
        @apply pl-3;
    }
    img {
        height: 50px;
        width: 50px;
    }

    .names {
        font-family: Lucida Caligraphy;
        color: #CC99E9;
        @apply text-lg;
    }
</style>
