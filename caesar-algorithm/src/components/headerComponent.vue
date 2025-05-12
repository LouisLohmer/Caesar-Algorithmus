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

  toggleTypewriterAnimation();
}

function toggleTypewriterAnimation() {
  console.log("hello there");
  let animatedElement1 = document.getElementById("animated-element");
  let animatedElement2 = document.getElementById("animated-element-2");
  let animatedElement3 = document.getElementById("animated-element-3");
  let animatedElement4 = document.getElementById("animated-element-4");
  let animatedElement5 = document.getElementById("animated-element-5");
  let animatedElement6 = document.getElementById("animated-element-6");

  if (!animatedElement1.classList.contains("typewriter-animaton")) {
    animatedElement1.classList.add("typewriter-animaton");
  } else {
    animatedElement1.classList.remove("typewriter-animaton");
  }

  if (!animatedElement2.classList.contains("typewriter-animaton")) {
    animatedElement2.classList.add("typewriter-animaton");
  } else {
    animatedElement2.classList.remove("typewriter-animaton");
  }

  if (!animatedElement3.classList.contains("typewriter-animaton")) {
    animatedElement3.classList.add("typewriter-animaton");
  } else {
    animatedElement3.classList.remove("typewriter-animaton");
  }

  if (!animatedElement4.classList.contains("typewriter-animaton")) {
    animatedElement4.classList.add("typewriter-animaton");
  } else {
    animatedElement4.classList.remove("typewriter-animaton");
  }

  if (!animatedElement5.classList.contains("typewriter-animaton")) {
    animatedElement5.classList.add("typewriter-animaton");
  } else {
    animatedElement5.classList.remove("typewriter-animaton");
  }

  if (!animatedElement6.classList.contains("typewriter-animaton")) {
    animatedElement6.classList.add("blink-caret-animation");
  } else {
    animatedElement6.classList.remove("blink-caret-animation");
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
