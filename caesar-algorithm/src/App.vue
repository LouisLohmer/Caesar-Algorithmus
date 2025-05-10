<script setup>
import headerComponent from "./components/headerComponent.vue";
import footerComponent from "./components/footerComponent.vue";
import startScreenComponent from "./components/startScreenComponent.vue";
import decryptTextComponent from "./components/decryptTextComponent.vue";
import encryptTextComponent from "./components/encryptTextComponent.vue";
</script>

<template>
  <headerComponent></headerComponent>
  <startScreenComponent></startScreenComponent>
  <div class="main-content hidden" id="main-content">
    <decryptTextComponent></decryptTextComponent>
    <encryptTextComponent></encryptTextComponent>
  </div>
  <footerComponent></footerComponent>
</template>

<style scoped>
.main-content {
  margin: auto 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 25px 15px 25px;
}
</style>
