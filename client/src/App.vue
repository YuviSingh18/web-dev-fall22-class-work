<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavVue from './components/Nav.vue';
</script>

<template>
  <NavVue />

  <div class="container">
    <RouterView />
  </div>
</template>
