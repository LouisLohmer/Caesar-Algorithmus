<script setup>
import headerComponent from "./components/headerComponent.vue";
import footerComponent from "./components/footerComponent.vue";
import startScreenComponent from "./components/startScreenComponent.vue";
import decryptTextComponent from "./components/decryptTextComponent.vue";
import encryptTextComponent from "./components/encryptTextComponent.vue";
import textComponent from "./components/textComponent.vue";
</script>

<template>
  <headerComponent></headerComponent>
  <startScreenComponent></startScreenComponent>
  <div class="main-content hidden" id="main-content">
    <textComponent></textComponent>
    <div class="sub-main-content">
      <decryptTextComponent></decryptTextComponent>
      <encryptTextComponent></encryptTextComponent>
    </div>
  </div>
  <footerComponent></footerComponent>
</template>

<style scoped>
.sub-main-content {
  margin: auto 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 15px 25px 15px 25px;
}

.main-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 50px;
}

/*Media-Querie for smart phones*/
@media only screen and (max-width: 767px) {
  .sub-main-content {
    flex-direction: column;
  }
}

/*Media-Querie for tablets*/
@media only screen and (min-width: 768px) and (max-width: 1023px) {
}
</style>
