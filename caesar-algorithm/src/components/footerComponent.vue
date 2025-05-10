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
        <img src="../assets/github-logo.png" class="github-logo" />
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
  border-radius: 20px;
  padding: 15px 25px 15px 25px;
  margin: 100px 25px 0 25px;
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
</style>
