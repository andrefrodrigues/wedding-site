<script lang="ts" setup>

</script>
<template>
    <section class="accomodation" id="accomodation">
        <a href="#accomodation">
            <h1 class="title"><img src="hotel.png" class="hotel-icon">Onde ficar</h1>
        </a>
    </section>
</template>
<style lang="postcss" scoped>
.accomodation {
    height: calc(100vh - 60px);
    @apply bg-indigo-200;
    @apply pt-10;
}


.title {
    @apply text-5xl;
    @apply flex items-center justify-center;

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
