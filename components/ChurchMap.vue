<template>
    <div class="church-map">
        <a href="https://maps.google.pt/maps?q=S%C3%A9%20Catedral%20de%20braga&t=&z=17&ie=UTF8&iwloc=">
            <img src="mapa-se.png">
        </a>
    </div>
</template>
<style scoped lang="postcss">
.church-map {
    @apply relative;
    z-index: 1;
    width: 200px;
    height: 200px;
    @apply mx-auto my-0;

    @media screen(sm) {
        width: 350px;
        height: 350px;
    }
}

a {
    @apply inline-block;
}
</style>
