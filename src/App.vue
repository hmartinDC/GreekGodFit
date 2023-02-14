<script setup>
import { RouterLink, RouterView } from "vue-router";
import HeaderGreek from "./components/HeaderGreek.vue";
import FooterGreek from "./components/FooterGreek.vue";
</script>

<template>
  <HeaderGreek />
  <RouterView></RouterView>
  <FooterGreek />
</template>
