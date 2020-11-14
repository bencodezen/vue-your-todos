<template>
  <main class="main-wrapper">
    <h1 class="page-title">Vue Your Todo</h1>
    <p class="subtitle">A todo app powered by Vue.js 3</p>
    <div class="new-task-wrapper">
      <input
        type="text"
        placeholder="Type a new todo item"
        class="new-task-input"
      />
      <button class="new-task-button">+ Add</button>
    </div>
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

.new-task-wrapper {
  display: flex;
}

.new-task-input {
  padding: 16px;
  font-weight: 600;
  color: #959595;
  flex: 1;
  border-top-left-radius: 8px;
  border-bottom-left-radius: 8px;
  border: 1px solid #f6f6f6;
  box-shadow: 2px 2px 8px 0 #c0c0c0;
  letter-spacing: 1px;
}

.new-task-button {
  background-color: #0631f8;
  color: #fff;
  padding: 18px 24px;
  font-weight: 900;
  border: 0;
  border-top-right-radius: 8px;
  border-bottom-right-radius: 8px;
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
  letter-spacing: 0.67px;
}
</style>
