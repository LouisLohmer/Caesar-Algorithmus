<script setup></script>

<template>
  <div>
    <footer>
      <span class="watermark"
        >Made by LonelyStreetracer with <span class="heart">❤</span></span
      >
      <a
        href="https://github.com/LouisLohmer/Caesar-Algorithmus"
        target="_blank"
        class="repositry-link"
      >
        Checkout the repository</a
      >
    </footer>
  </div>
</template>

<style scoped>
.watermark {
  font-size: var(--text-font);
  font-family: monospace;
  margin-right: 20px;
}

.heart {
  color: var(--red);
  font-size: var(--big-text-font);
}

footer {
  border-top: 3px solid var(--dark-grey);
  margin: 10px 25px 10px 25px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.repositry-link {
  border-left: 3px solid var(--dark-grey);
  font-size: var(--text-font);
  color: var(--white);
  padding-left: 20px;
  text-decoration: none;
}
.repositry-link:hover {
  color: var(--green);
}
</style>
