<script setup>
import { onMounted } from "vue";

onMounted(() => {
  fetch("https://jsonplaceholder.typicode.com/posts/1")
    .then((r) => r.json())
    .then((r) => console.log(r));
});
</script>

<template>
  <div id="app">
    <header>
      <img
        alt="AAWZ Tecnologia"
        class="logo"
        src="https://aawz.com.br/_nuxt/img/logo-tecnologia.d3a696c.png"
        height="55"
      />
    </header>

    <router-view />
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
