<script setup>
import BlubComponent from "../components/BlubComponent.vue";
</script>

<template>
  <main>
    <div>
      <h2>Welcome to the world of web development!</h2>
    </div>
    <BlubComponent :top="50" :left="50" :rotate="150" />
    <BlubComponent :top="50" :left="50" :rotate="120" />
    <BlubComponent :top="50" :left="50" :rotate="135" />
  </main>
</template>

<style scoped>
h2 {
  color: #f2f2f2;
  text-align: center;
}
main {
  display: flex;
  position: relative;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  min-height: calc(100vh - 60px);
  overflow: hidden;
}
</style>
