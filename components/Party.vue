<script lang="ts" setup>

</script>
<template>
    <section class="party" id="party">
        <div class="content">
            <a href="#party">
                <h1 class="title"><img class="popper" src="party-popper.png">Festa</h1>
            </a>
            <div class="card-wrapper">
                <a href="https://www.torredanaia.com/">
                    <div class="card">
                        <h2 class="card-title">Torre da Naia</h2>
                        <img class="card-img" src="torre-da-naia-entrada.jpeg">
                    </div>
                </a>
                <a href="https://maps.google.com/maps?q=torre%20da%20naia&t=&z=13&ie=UTF8&iwloc">
                    <div class="card">
                        <h2 class="card-title">Localização</h2>
                        <img class="card-img" src="naia-map.png">
                    </div>
                </a>
        </div>
        </div>
    </section>
</template>

<style lang="postcss" scoped>
.party {
    @apply text-center;
    @apply p-10;
    height: calc(100vh - 60px);
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
    @apply -mx-10;
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

.card {
    @apply mt-12;
    @apply relative;
    transition: all 500ms;

    @media screen(sm) {
        @apply mt-0;
    }
}

.card:hover {
    transform: scale(1.2);
}

.card:hover > .card-img {
    filter: none;
}

.card:hover > .card-title {
    @apply bg-indigo-200;
}

.card-title {
    transition: background-color 500ms;
    @apply w-full;
    @apply text-3xl;
    @apply absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2;
    z-index: 1;
}

.card-img {
    filter: brightness(50%);
    width: 450px;
}

</style>
