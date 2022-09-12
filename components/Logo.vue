<template>
    <Anchor class="logo" id="hero">
        <img src="lavender.png"/>
        <span class="names">Elisa & André</span>
    </Anchor>
</template>

<style lang="postcss" scoped>
    .logo {
        @apply flex items-center;

        @media screen(sm) {
            @apply absolute;
        }
    }
    img {
        height: 50px;
        width: 50px;
    }

    .names {
        font-family: Charm;
        color: #CC99E9;
        @apply text-2xl;
    }
</style>
