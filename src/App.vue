<template>
  <main class="main-wrapper">
    <h1 class="page-title">Vue Your Todo</h1>
    <p class="subtitle">A todo app powered by Vue.js 3</p>
    <input type="text" />
    <button>+ Add</button>
  </main>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
html {
  background-color: #fbfbfb;
}

.main-wrapper {
  max-width: 600px;
  margin: 0 auto;
}

.page-title {
  font-family: 'DM Serif Display', serif;
  font-size: 44px;
  letter-spacing: 1.84px;
  color: #2d2d2d;
  margin-top: 104px;
  margin-bottom: 0;
}

.subtitle {
  font-size: 1rem;
  font-weight: bold;
  color: #6b6b6b;
  margin-top: 0;
}
</style>
