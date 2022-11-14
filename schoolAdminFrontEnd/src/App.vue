<script setup>
import { RouterView } from "vue-router";
import NavBar from "./views/Navbar.vue";
</script>

<template>
  <NavBar />
  <div class="background"></div>
  <div class="foreground">
    <RouterView />
  </div>
</template>
