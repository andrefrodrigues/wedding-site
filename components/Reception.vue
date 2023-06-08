<script lang="ts" setup>

</script>
<template>
  <section class="reception" id="reception">
    <div class="content">
      <p class="message">Antes da cerimónia religiosa passem pela casa dos pais da Elisa e venham petiscar qualquer coisa e brindar connosco.</p>
      <p class="message">Apareçam a partir das 9h30</p>
      <div class="card-wrapper">
        <a href="https://goo.gl/maps/Nm8kocf4aXdocdk67" target="_blank">
          <Card title="Localização" image="casa-pais-elisa.png"/>
        </a>
      </div>
    </div>
  </section>
</template>
<style lang="postcss" scoped>
.reception {
    scroll-margin-top: 60px;
    height: 550px;
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

.message {

  @media screen(md) {
    @apply w-1/2;
    @apply text-3xl; 
    @apply leading-10;
  }

  @apply text-2xl;
  @apply mx-auto;
  @apply text-center;
}

.reception::after {
  content: "";
  background-image: url("https://images.unsplash.com/photo-1522413452208-996ff3f3e740?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3600&q=80");
  display: block;
  position: absolute;
  height: 550px;
  width: 100%;
  filter: brightness(60%);
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

.card-wrapper {

 @media screen(sm) {
  @apply mt-10;
 }

  @apply flex;
  @apply justify-center; 
}
</style>
