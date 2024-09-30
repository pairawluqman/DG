<template>
  <div class="min-h-screen">
    <TopBar />
    <Slider v-if="!nav" />
    <Info />
    <Card />
    <ourService />
  </div>
</template>

<script setup>
import Slider from "~/components/slider/Slider.vue";
import TopBar from "~/layouts/TopBar.vue";
import Info from "~/components/Info/Info.vue";
import Card from "~/components/card/Card.vue";
import ourService from "~/components/ourService/index.vue";
</script>
