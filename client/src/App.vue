<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import NavVue from './components/Nav.vue';
</script>

<template>
  <NavVue />
  <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
  

  <div class="container">
    <RouterView />
  </div>
</template>
