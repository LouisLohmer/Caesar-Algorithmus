<script setup></script>

<template>
  <div>
    <footer>
      <span class="watermark"
        >Made by LonelyStreetracer with <span class="heart">❤</span></span
      >
      <div class="social-media-link-container">
        <a
          href="https://github.com/LouisLohmer/Caesar-Algorithmus"
          target="_blank"
          class="repositry-link"
        >
          Checkout the repository</a
        >
        <img src="../assets/images/github-logo.png" class="github-logo" />
      </div>
    </footer>
  </div>
</template>

<style scoped>
.watermark {
  font-size: var(--text-font);
  font-family: monospace;
  margin-right: 20px;
  color: var(--marble-white);
}

.heart {
  color: var(--red);
  font-size: var(--big-text-font);
}

footer {
  border-top: 3px solid var(--imperial-gold);
  outline: 3px solid var(--royalblue);
  border-radius: 20px;
  padding: 15px 25px 15px 25px;
  margin: 120px 25px 0 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
}

.repositry-link {
  border-left: 3px solid var(--marble-white);
  font-size: var(--text-font);
  color: var(--marble-white);
  padding-left: 20px;
  text-decoration: none;
}
.repositry-link:hover {
  color: var(--imperial-gold);
}

.github-logo {
  height: 35px;
  width: 35px;
}

.social-media-link-container {
  display: flex;
  align-items: center;
  gap: 10px;
}

/*Media-Querie for smart phones*/
@media only screen and (max-width: 767px) {
  footer {
    flex-direction: column;
    padding: 20px 5px 20px 5px;
  }

  .repositry-link {
    border-left: 0;
    padding-left: 0;
  }

  .social-media-link-container {
    padding: 10px 0 10px 0;
  }

  .watermark {
    padding: 10px 0 10px 0;
    border-bottom: 3px solid var(--marble-white);
    margin: 0;
  }
}

/*Media-Querie for tablets*/
@media only screen and (min-width: 768px) and (max-width: 1023px) {
}
</style>
