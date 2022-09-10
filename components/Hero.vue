<template>
    <section class="hero">
        <h1 class="names">
            <a href="#">
                <div>
                    Elisa Beatriz
                </div>
                <div>
                    &
                </div>
                <div>André Filipe</div>
                <h2 class="date">
                    <img src="lavender.png"><span>19 de agosto de 2023</span><img src="lavender.png" class="right-lavander">
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
    background-image: linear-gradient(180deg, #a5b4fc, transparent 23%), linear-gradient(180deg, transparent 47%, #a5b4fc), url('static/hero-pic-mobile.jpeg');
    background-position: center;
    background-repeat: no-repeat;
    filter: grayscale(50%);
    background-size: cover;

    @media screen(md) {
        background-image: linear-gradient(180deg, #a5b4fc, transparent 23%), linear-gradient(180deg, transparent 47%, #a5b4fc), url('static/hero-pic.jpeg');
        background-size: cover;
        background-position: top;
        box-shadow: -1px -10px 21px 0px rgba(165, 180, 252, 0.75) inset;
    }
}

.names {
    font-family: Lucida Caligraphy;
    @apply w-full;
    @apply font-bold;
    @apply text-gray-100;
    @apply text-center;
    @apply absolute left-1/2;
    transform: translate(-50%);
    font-size: 28px;
    bottom: 70px;

    @media screen(md) {
        bottom: 50px;
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
