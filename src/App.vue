<script setup lang="ts">
import Home from './pages/Home/Home.vue';

</script>

<template>
  <main class="layout">
    <Home/>
  </main>
</template>

<style scoped>

.layout{
  box-sizing: content-box;
}

header {
  line-height: 1.5;
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

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
