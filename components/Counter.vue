<script lang="ts" setup>
import { ref, computed } from 'vue';

const weddingDate = '2023-08-19';
const now = ref(new Date());

const prefixZero = (v: number): string => {
    if (v > 9) {
        return `${v}`;
    }

    return `0${v}`;
};

const totalLeft = computed(() => {
    const total = Date.parse(weddingDate) - Date.parse(now.value.toUTCString());
    if (total < 0) {
        return 0;
    }
    return total;
});

const days = computed(() => prefixZero(Math.floor(totalLeft.value / (1000 * 60 * 60 * 24))));
const hours = computed(() => prefixZero(Math.floor((totalLeft.value / (1000 * 60 * 60)) % 24)));
const minutes = computed(() => prefixZero(Math.floor((totalLeft.value / 1000 / 60) % 60)));
const seconds = computed(() => prefixZero(Math.floor((totalLeft.value / 1000) % 60)));
setInterval(() => {
    now.value = new Date();
}, 1000);

</script>
<template>
    <section class="counter">
        <div class="timer">
            <div>
                <span class="unit">{{days}}</span>
                <div class="label">Dias</div>
            </div>
            <div class="splitter">
                :
            </div>
            <div>
                <span class="unit">{{hours}}</span>
                <div class="label">Horas</div>
            </div>
            <div class="splitter">
                :
            </div>
            <div>
                <span class="unit">{{minutes}}</span>
                <div class="label">Minutos</div>
            </div>
            <div class="splitter">
                :
            </div>
            <div>
                <span class="unit">{{seconds}}</span>
                <div class="label">segundos</div>
            </div>
        </div>
    </section>
</template>

<style lang="postcss" scoped>
.counter {
    @apply relative;
    @apply bg-indigo-200;
    height: 250px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.timer {
    @apply absolute top-1/2 left-1/2;
    transform: translate(-50%, -50%);
    @apply flex;
    @apply items-start justify-center;
    ;
}

.unit {
    @apply text-4xl;
    font-feature-settings: "tnum";
    font-variant-numeric: tabular-nums;

    @media screen(md) {
        @apply text-5xl;
    }
}

.label {
    @apply text-center;
    font-size: 10px;

    @media screen(md) {
        @apply text-xs;
    }
}

.splitter {
    @apply text-4xl;
    @apply mx-4 pb-4;

    @media screen(md) {
        @apply text-5xl;
    }
}
</style>
