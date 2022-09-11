<script lang="ts" setup>

</script>
<template>
    <section class="party" id="party">
        <div class="content">
            <a href="#party">
                <h1 class="title"><img class="popper" src="party-popper.png">Festa</h1>
            </a>
            <div class="card-wrapper">
                <a href="https://www.torredanaia.com/" target="_blank">
                    <Card title="Torre da Naia" image="torre-da-naia-entrada.jpeg"/>
                </a>
                <a href="https://maps.google.com/maps?q=torre%20da%20naia&t=&z=13&ie=UTF8&iwloc" target="_blank">
                    <Card title="Localização" image="naia-map.png" />
                </a>
        </div>
        </div>
    </section>
</template>

<style lang="postcss" scoped>
.party {
    scroll-margin-top: 60px;
    @apply text-center;
    @apply p-9;
    height: 100vh;
    @apply bg-indigo-300;
    @apply relative;
}


.party::after {
    content: "";
    display: block;
    position: absolute;
    height: 100%;
    width: 100%;
    background-image: url('static/torre-da-naia.jpeg');
    background-size: cover;
    background-position: top;
    top: 0;
    opacity: 0.6;
    filter: brightness(50%);
    @apply -mx-9;
}

.title {
    @apply text-5xl;
    @apply flex items-center justify-center;

    @media screen(md) {
        @apply text-6xl;
    }
}

.popper {
    display: inline;
    width: 48px;
    height: 48px;
    @apply mr-2;
}

.content {
    @apply relative;
    z-index: 1;
}

.card-wrapper {
    @apply flex flex-col justify-around;

    @media screen(sm) {
        @apply w-full;
        @apply mt-64;
        @apply flex-row;
    }
}
</style>
