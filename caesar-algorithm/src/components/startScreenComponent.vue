<script setup></script>

<template>
  <div class="image-constellation-container" id="image-constellation">
    <img
      src="../assets/images/caesar-cipher-2.png"
      class="caesar-cipher-background-image"
    />
    <img src="../assets/images/caesar-cipher.png" class="caesar-cipher-image" />
    <img
      src="../assets/images/caesar-statue.png"
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

.image-constellation-container {
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
  transition: all 5s ease-out;
}

.caesar-cipher-background-image {
  left: 10%;
  top: 50px;
}
.caesar-cipher-background-image:hover,
.caesar-cipher-background-image-2:hover {
  transition: all 5s ease-out;
  filter: blur(0px);
  cursor: pointer;
}

.caesar-cipher-background-image-2 {
  right: 10%;
  top: 50px;
}

/*Media-Querie for smart phones*/
@media only screen and (max-width: 767px) {
  .caesar-cipher-image {
    width: 45%;
    height: 45%;
  }

  .caesar-cipher-background-image-2,
  .caesar-cipher-background-image {
    width: 45%;
    height: 45%;
  }

  .caesar-cipher-background-image {
    left: 22%;
    top: 30px;
  }

  .caesar-cipher-background-image-2 {
    left: -22%;
    top: 30px;
  }
}

/*Media-Querie for tablets*/
@media only screen and (min-width: 768px) and (max-width: 1023px) {
  .caesar-cipher-image {
    width: 50%;
    height: 50%;
  }

  .caesar-cipher-background-image-2,
  .caesar-cipher-background-image {
    width: 50%;
    height: 50%;
  }

  .caesar-cipher-background-image {
    left: 27%;
    top: 30px;
  }

  .caesar-cipher-background-image-2 {
    left: -27%;
    top: 30px;
  }
}
</style>
