<script lang="ts" setup>
import { computed } from 'vue';

const hotelData = [
    { id: 1, name: 'Urban Hotel estação', url: 'https://www.booking.com/hotel/pt/estacao.pt-pt.html', image: 'urban-hotel.jpeg' },
    { id: 2, name: 'Basic Braga by Axis', url: 'https://www.booking.com/hotel/pt/basic-by-axis.pt-pt.html', image: 'basic-braga.jpeg' },
    { id: 3, name: 'Hotel do Lago', url: 'https://www.booking.com/hotel/pt/do-lago.pt-pt.html', image: 'hotel-do-lago.jpeg' },
    { id: 4, name: 'Ibis Budget Braga Centro', url: 'https://www.booking.com/hotel/pt/ibis-budget-braga-centro.pt-pt.html', image: 'ibis-budget.jpeg' },
    { id: 5, name: 'Ibis Braga', url: 'https://www.booking.com/hotel/pt/ibis-braga.pt-pt.html', image: 'ibis-braga.jpeg' }
]

const hotels = computed(() => hotelData.sort((h1, h2) => h1.name.localeCompare(h2.name)));
</script>
<template>
    <section class="accomodation" id="accomodation">
        <div class="content">
            <Anchor id="accomodation">
                <h1 class="title"><img src="hotel.png" class="hotel-icon">Onde ficar</h1>
            </Anchor>

            <div class="card-container">
                <a v-for="hotel in hotels" :key="hotel.id" :href="hotel.url" class="card-wrapper" target="_blank">
                    <Card :title="hotel.name" :image="hotel.image" />
                </a>
            </div>
        </div>
    </section>
</template>
<style lang="postcss" scoped>
.card-wrapper {

    @media screen(sm) {
        @apply pt-20 pl-20;
    }
}

.card-container {
    @apply flex flex-col flex-wrap;
    @apply w-full;

    @media screen(sm) {
        @apply -mt-20 -ml-20;
        @apply mx-auto;
        @apply w-full;
        @apply flex-row;
    }
}

.accomodation {
    scroll-margin-top: 60px;
    min-height: calc(100vh - 60px);
    @apply bg-indigo-200;
    @apply py-10;
    @apply px-9;
    @apply relative;

    @media screen(sm) {
        @apply px-20;
    }
}

.content {
    @apply relative;
    z-index: 1;
}

.accomodation::after {
    content: "";
    display: block;
    position: absolute;
    height: 100%;
    width: 100%;
    background-image: url('https://images.unsplash.com/photo-1512918728675-ed5a9ecdebfd?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3570&q=80');
    filter: brightness(80%);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    top: 0;
    opacity: 0.6;
    @apply -mx-9;

    @media screen(sm) {
        @apply -mx-20;
    }
}


.title {
    white-space: nowrap;

    @apply text-5xl;
    @apply flex items-center justify-center;
    @apply mb-16;

    @media screen(md) {
        @apply text-6xl;
    }
}

.hotel-icon {
    display: inline;
    width: 48px;
    height: 48px;
    @apply mr-2;
}
</style>
