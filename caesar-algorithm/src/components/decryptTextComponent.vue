<script setup>
function encryptText() {
  let alphabet = [
    "a",
    "b",
    "c",
    "d",
    "e",
    "f",
    "g",
    "h",
    "i",
    "j",
    "k",
    "l",
    "m",
    "n",
    "o",
    "p",
    "q",
    "r",
    "s",
    "t",
    "u",
    "v",
    "w",
    "x",
    "y",
    "z",
  ];
  const onlyLettersRegEx = /^[a-zA-Z]+$/;
  let textareaElement = document.getElementById("encryption-textarea");
  let decryptedText = textareaElement.value.split("");
  let optionElements = document.getElementById("select-encryption-key").options;
  let encryptionKey = optionElements[optionElements.selectedIndex].id;
  let encryptedTextElement = document.getElementById("encrypted-text");
  let encryptedText = "";
  let copyToClipboardButton = document.getElementById("copy-to-clipboard-2");

  for (let i = 0; i < decryptedText.length; i++) {
    let decryptedLetter = decryptedText[i].toLowerCase();
    let indexDecryptedLetter = alphabet.indexOf(decryptedLetter);

    if (!decryptedLetter.match(onlyLettersRegEx)) {
      encryptedText = encryptedText += decryptedLetter;
    } else {
      for (let a = 0; a < encryptionKey; a++) {
        if (indexDecryptedLetter === 0) {
          indexDecryptedLetter = 25;
        } else {
          indexDecryptedLetter--;
        }
      }

      encryptedText = encryptedText += alphabet[indexDecryptedLetter];
    }
  }

  encryptedTextElement.innerHTML = encryptedText;
  copyToClipboardButton.style.visibility = "visible";
}

function validateUserInput() {
  let errorMessageElement = document.getElementById("error-message");
  let textareaElement = document.getElementById("encryption-textarea");
  let text = textareaElement.value;
  let optionElements = document.getElementById("select-encryption-key").options;
  let idSelectedOptionElement = optionElements[optionElements.selectedIndex].id;

  if (text.length === 0) {
    errorMessageElement.innerHTML = "Das Textfeld darf nicht leer sein!";
    return;
  } else {
    errorMessageElement.innerHTML = "";
  }

  if (idSelectedOptionElement === "null") {
    errorMessageElement.innerHTML = "Wähle bitte einen validen Schlüssel aus!";
    return;
  } else {
    errorMessageElement.innerHTML = "";
  }

  encryptText();
}

function copyEncryptedTextToClipboard() {
  let encryptedText = document.getElementById("encrypted-text").innerHTML;
  let successsMessage = document.getElementById("success-message-2");

  navigator.clipboard.writeText(encryptedText);
  successsMessage.classList.remove("hidden");

  setTimeout(() => {
    console.log("Waited 5 seconds!");
    successsMessage.classList.add("hidden");
  }, 5000);
}
</script>

<template>
  <div class="encryption-container">
    <h2>Text entschlüsseln</h2>
    <textarea
      id="encryption-textarea"
      placeholder="Gebe deinen verschlüsselten Text hier ein..."
    ></textarea>
    <span class="error-message" id="error-message"></span>
    <div class="interactive-encryption-elements">
      <button class="encrypt-text" @click="validateUserInput">
        entschlüsseln
      </button>
      <select class="choose-encryption-key" id="select-encryption-key">
        <option id="null">Wähle einen Schlüssel aus!</option>
        <option id="3">3</option>
        <option id="4">4</option>
        <option id="5">5</option>
        <option id="6">6</option>
        <option id="7">7</option>
        <option id="8">8</option>
        <option id="9">9</option>
        <option id="10">10</option>
        <option id="11">11</option>
        <option id="12">12</option>
        <option id="13">13</option>
        <option id="14">14</option>
        <option id="15">15</option>
        <option id="16">16</option>
        <option id="17">17</option>
        <option id="18">18</option>
        <option id="19">19</option>
        <option id="20">20</option>
        <option id="21">21</option>
        <option id="22">22</option>
        <option id="23">23</option>
        <option id="24">24</option>
        <option id="25">25</option>
      </select>
    </div>
    <div class="encrypyeted-text-container">
      <h2>Entschlüsselter Text</h2>
      <span class="success-message hidden" id="success-message-2"
        >Text kopiert!</span
      >
      <div class="result-container">
        <button
          class="copy-to-clipboard"
          id="copy-to-clipboard-2"
          @click="copyEncryptedTextToClipboard"
        >
          <svg
            class="copy-to-clipboard-icon"
            clip-rule="evenodd"
            fill-rule="evenodd"
            stroke-linejoin="round"
            stroke-miterlimit="2"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="m6 19v2c0 .621.52 1 1 1h2v-1.5h-1.5v-1.5zm7.5 3h-3.5v-1.5h3.5zm4.5 0h-3.5v-1.5h3.5zm4-3h-1.5v1.5h-1.5v1.5h2c.478 0 1-.379 1-1zm-1.5-1v-3.363h1.5v3.363zm0-4.363v-3.637h1.5v3.637zm-13-3.637v3.637h-1.5v-3.637zm11.5-4v1.5h1.5v1.5h1.5v-2c0-.478-.379-1-1-1zm-10 0h-2c-.62 0-1 .519-1 1v2h1.5v-1.5h1.5zm4.5 1.5h-3.5v-1.5h3.5zm3-1.5v-2.5h-13v13h2.5v-1.863h1.5v3.363h-4.5c-.48 0-1-.379-1-1v-14c0-.481.38-1 1-1h14c.621 0 1 .522 1 1v4.5h-3.5v-1.5z"
              fill-rule="nonzero"
            />
          </svg>
        </button>
        <span class="encrypted-text" id="encrypted-text"></span>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
