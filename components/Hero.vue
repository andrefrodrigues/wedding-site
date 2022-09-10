<template>
    <section class="hero">
        <h1 class="names">
            <a href="#">
                <div>Elisa Beatriz & André Filipe</div>
                <h2 class="date">
                    <span>19 de agosto de 2023</span>
                </h2>
            </a>
        </h1>
    </section>
</template>
<style lang="postcss" scoped>
.hero {
    animation: fadeIn 1.5s;
    @apply relative;
    height: 100vh;
    background-image: linear-gradient(180deg, #a5b4fc, transparent 23%), url('static/hero-pic-mobile.jpeg');
    background-position: center;
    background-repeat: no-repeat;
    filter: grayscale(50%);
    background-size: cover;

    @media screen(md) {
        background-image: linear-gradient(180deg, #a5b4fc, transparent 23%), url('static/hero-pic.jpeg');
        background-size: cover;
        background-position: top;
        box-shadow: -1px -10px 21px 0px rgba(165, 180, 252, 0.75) inset;
    }
}

.names {
    font-family: Charm;
    @apply w-full;
    @apply font-bold;
    @apply text-gray-100;
    @apply text-center;
    @apply absolute left-1/2;
    transform: translate(-50%);
    @apply text-2xl;
    bottom: 50px;

    @media screen(md) {
        @apply text-5xl;
    }
}

.date {
    @apply mt-6;
    @apply flex items-center justify-center;
}

img {
    width: 64px;
    height: 64px;
}

.right-lavander {
    transform: rotateY(180deg);
}
</style>
