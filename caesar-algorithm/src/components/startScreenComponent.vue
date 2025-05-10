<script setup></script>

<template>
  <header>
    <nav>
      <h1>Caesar-Algorithmus</h1>

      <div>
        <button class="closeStartScreen">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 32 32"
            class="arrow-icon-forward"
          >
            <path
              d="m26.71 10.29-10-10a1 1 0 0 0-1.41 0l-10 10 1.41 1.41L15 3.41V32h2V3.41l8.29 8.29z"
            />
          </svg>
        </button>
        <button class="openStartScreen">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 32 32"
            class="arrow-icon-backwards"
          >
            <path
              d="m26.71 10.29-10-10a1 1 0 0 0-1.41 0l-10 10 1.41 1.41L15 3.41V32h2V3.41l8.29 8.29z"
            />
          </svg>
        </button>
      </div>
    </nav>
  </header>
</template>

<style scoped>
.arrow-icon-forward {
  fill: var(--white);
  height: 30px;
  width: 30px;
  transform: rotate(90deg);
}

.arrow-icon-backwards {
  fill: var(--white);
  height: 30px;
  width: 30px;
  transform: rotate(270deg);
}

.closeStartScreen,
.openStartScreen {
  background-color: var(--gold);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 25px 10px 25px;
}

h1 {
  color: var(--green);
}
</style>
