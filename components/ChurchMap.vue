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
    width: 100%;
    max-width: 500px;
    @apply mx-auto my-0;

    @media screen(sm) {
        filter: brightness(50%);
        transition: all 500ms;
        width: 300px;
        height: 300px;
    }
}

.church-map:hover {
    transform: scale(1.4);
    filter: none;
}

a {
    @apply inline-block;
}
</style>
