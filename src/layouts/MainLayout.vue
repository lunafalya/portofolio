<template>
  <section class="home">
    <h1>Hi, I'm {{ name }}</h1>
    <p>{{ tagline }}</p>
  </section>
</template>

<script setup>
import { ref } from "vue";

const name = ref("Nama Kamu");
const tagline = ref("Web Developer | Mobile Developer | Designer");
</script>

<style scoped>
.home {
  padding: 80px 20px;
  text-align: center;
}
h1 {
  font-size: 48px;
  margin-bottom: 10px;
}
</style>
