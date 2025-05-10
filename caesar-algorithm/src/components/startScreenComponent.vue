<script setup></script>

<template>
  <div class="centered-container">
    <img
      src="../assets/caesar-cipher-2.png"
      class="caesar-cipher-background-image"
    />
    <img src="../assets/caesar-cipher.png" class="caesar-cipher-image" />
    <img
      src="../assets/caesar-statue.png"
      class="caesar-cipher-background-image-2"
    />
  </div>
</template>

<style scoped>
.caesar-cipher-image {
  border-radius: 20px;
  width: 30%;
  height: 30%;
  z-index: 20;
}

.centered-container {
  margin: auto 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.caesar-cipher-background-image-2,
.caesar-cipher-background-image {
  position: relative;
  border-radius: 20px;
  width: 30%;
  height: 30%;
  z-index: 10;
  filter: blur(8px);
}

.caesar-cipher-background-image {
  left: 220px;
  top: 50px;
}

.caesar-cipher-background-image-2 {
  right: 220px;
  top: 50px;
}
</style>
