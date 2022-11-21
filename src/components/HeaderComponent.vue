<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <header>
    <RouterLink to="/">TheLostOrder</RouterLink>
    <nav>
      <ul class="navbar">
        <li><RouterLink to="/about_me">About me</RouterLink></li>
        <li><RouterLink to="/projects">Projects</RouterLink></li>
        <li><RouterLink to="/contacts">Contacts</RouterLink></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  padding: 0.85rem 10%;
  max-height: 60px;
  background-color: #181818;
}
header > a {
  background: -webkit-linear-gradient(60deg, #8758ff, #5cb8e4);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  font-size: 2rem;
}
header,
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.navbar a {
  color: #f2f2f2;
  text-decoration: none;
  font-size: 1.25rem;
  transition: 0.2s all ease-in-out;
  border-bottom: 1px solid #181818;
  padding: 10px 0;
}
.navbar a:hover {
  color: #8758ff;
  border-bottom-width: 2px;
  border-bottom-color: #5cb8e4;
}
.navbar {
  list-style: none;
}
nav {
  width: 35%;
}
</style>
