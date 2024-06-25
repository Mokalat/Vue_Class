<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <!-- <RouterLink to="/about">Pinia설명</RouterLink> -->
        <RouterLink to="post">Post추가란</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  display: flex;
  flex-direction: column;
  align-items: center;
}
body {
  background-color: rgb(110, 110, 110);
}
a {
  margin-left: 10px;
  font-size: 20px;
}
</style>
