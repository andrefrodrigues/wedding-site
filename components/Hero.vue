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
            </a>
        </h1>
    </section>
</template>
<style lang="postcss" scoped>
.hero {
    animation: fadeIn 1.5s;
    @apply relative;
    height: calc(100vh - 60px);
    background-image: linear-gradient(180deg, #a5b4fc, transparent 23%), linear-gradient(180deg, transparent 47%, #a5b4fc), url('static/hero-pic-mobile.jpeg');
    background-position: center;
    background-repeat: no-repeat;
    filter: grayscale(50%);
    background-size: cover;

    @media screen(md) {
        background-image: linear-gradient(180deg, #a5b4fc, transparent 23%), linear-gradient(180deg, transparent 47%, #a5b4fc), url('static/hero-pic.jpeg');
        background-size: cover;
        background-position: top;
        box-shadow: -1px -20px 21px 0px rgba(165,180,252,0.75) inset;
    }
}
.names {
    font-family: Lucida Caligraphy;
    @apply font-bold;
    @apply text-gray-100;
    @apply text-center;
    @apply absolute top-1/2 left-1/2;
    transform: translate(-50%, calc(150px - 60px));
    font-size: 28px;

    @media screen(md) {
        @apply text-5xl;
        transform: translate(-50%, 20px);
    }

}
</style>
