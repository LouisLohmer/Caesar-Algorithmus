<script setup>
function toggleVisibilityOfStartScreen() {
  let imageConstellationContainer = document.getElementById(
    "image-constellation"
  );
  let closeStartScreenButton = document.getElementById(
    "close-start-screen-button"
  );
  let openStartScreenButton = document.getElementById(
    "open-start-screen-button"
  );
  let mainContentContainer = document.getElementById("main-content");

  if (!imageConstellationContainer.classList.contains("hidden")) {
    imageConstellationContainer.classList.add("hidden");
  } else {
    imageConstellationContainer.classList.remove("hidden");
  }

  if (!closeStartScreenButton.classList.contains("hidden")) {
    closeStartScreenButton.classList.add("hidden");
  } else {
    closeStartScreenButton.classList.remove("hidden");
  }

  if (!openStartScreenButton.classList.contains("hidden")) {
    openStartScreenButton.classList.add("hidden");
  } else {
    openStartScreenButton.classList.remove("hidden");
  }

  if (!mainContentContainer.classList.contains("hidden")) {
    mainContentContainer.classList.add("hidden");
  } else {
    mainContentContainer.classList.remove("hidden");
  }

  toggleAnimations();
}

function toggleAnimations() {
  let firstAnimatedElement = document.getElementById("animated-element");
  let secondAnimatedElement = document.getElementById("animated-element-2");
  let thirdAnimatedElement = document.getElementById("animated-element-3");
  let fourthAnimatedElement = document.getElementById("animated-element-4");
  let fifthAnimatedElement = document.getElementById("animated-element-5");
  let sixthAnimatedElement = document.getElementById("animated-element-6");

  if (
    !firstAnimatedElement.classList.contains("typewriter-animaton") &&
    !secondAnimatedElement.classList.contains("typewriter-animaton") &&
    !thirdAnimatedElement.classList.contains("typewriter-animaton") &&
    !fourthAnimatedElement.classList.contains("typewriter-animaton") &&
    !fifthAnimatedElement.classList.contains("typewriter-animaton") &&
    !sixthAnimatedElement.classList.contains("typewriter-animaton")
  ) {
    firstAnimatedElement.classList.add("typewriter-animaton");
    secondAnimatedElement.classList.add("typewriter-animaton");
    thirdAnimatedElement.classList.add("typewriter-animaton");
    fourthAnimatedElement.classList.add("typewriter-animaton");
    fifthAnimatedElement.classList.add("typewriter-animaton");
    sixthAnimatedElement.classList.add("blink-caret-animation");
  } else {
    firstAnimatedElement.classList.remove("typewriter-animaton");
    secondAnimatedElement.classList.remove("typewriter-animaton");
    thirdAnimatedElement.classList.remove("typewriter-animaton");
    fourthAnimatedElement.classList.remove("typewriter-animaton");
    fifthAnimatedElement.classList.remove("typewriter-animaton");
    sixthAnimatedElement.classList.remove("blink-caret-animation");
  }
}
</script>

<template>
  <header>
    <nav>
      <h1>Caesar-Algorithmus</h1>

      <div>
        <button
          class="close-start-screen"
          id="close-start-screen-button"
          @click="toggleVisibilityOfStartScreen"
        >
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
        <button
          class="open-start-screen hidden"
          id="open-start-screen-button"
          @click="toggleVisibilityOfStartScreen"
        >
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
  fill: var(--marble-white);
  height: 30px;
  width: 30px;
  transform: rotate(90deg);
}

.arrow-icon-backwards {
  fill: var(--marble-white);
  height: 30px;
  width: 30px;
  transform: rotate(270deg);
}

.close-start-screen,
.open-start-screen {
  background-color: var(--royalblue);
}

.open-start-screen:hover .arrow-icon-backwards {
  fill: var(--imperial-gold);
}

.close-start-screen:hover .arrow-icon-forward {
  fill: var(--imperial-gold);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header {
  padding: 15px 25px 15px 25px;
  margin-bottom: 30px;
}
</style>
