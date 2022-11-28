<script setup lang="ts">
  const items = [
    { name: 'Shoes', cost: 30},
    { name: 'Shirt', cost: 20},
    { name: 'Pants', cost: 50},
    { name: 'Hat', cost: 10},
    { name: 'Socks', cost: 5}
  ]
</script>

<template>
  <div class="about">
    <h1 class="title">This is an about page</h1>
    <ul>
      <li v-for="item in items">
        {{ item.name }} - ${{ item.cost }}
      </li>
    </ul>
  </div>
</template>

