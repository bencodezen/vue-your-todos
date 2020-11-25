<template>
  <h1 :class="$style['page-title']">Vue Your Todo</h1>
  <p :class="$style.subtitle">
    A todo app powered by
    <a href="https://v3.vuejs.org/">Vue 3</a>
    <span>, </span>
    <a
      href="https://www.netlify.com/?utm_source=github&utm_medium=vueyourtodos-bh&utm_campaign=devex"
      >Netlify</a
    >
    <span> & </span>
    <a href="https://www.github.com/bencodezen/peek-a-vue"> GitHub</a>
  </p>
</template>

<style module>
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
  margin-bottom: 30px;
  letter-spacing: 0.67px;
}
</style>
