<script setup lang="ts">
import { ref } from "vue";

const boards = [
  {
    id: "1",
    title: "Vue.js",
    img: "https://placekitten.com/400/300",
  },
];
</script>

<template>
  <h1 class="mb-5 text-3xl">Boards</h1>
  <div v-for="{ id, title, img } in boards" :key="id">
    <!-- <div>{{ id }}</div> -->
    <div>{{ title }}</div>
    <img :src="img" />
  </div>
  <button @click="addBoard"></button>
</template>
