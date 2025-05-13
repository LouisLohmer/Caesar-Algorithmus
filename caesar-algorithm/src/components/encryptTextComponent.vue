<script setup>
function decryptText() {
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
  let textareaElement = document.getElementById("decryption-textarea");
  let encryptedText = textareaElement.value.split("");
  let optionElements = document.getElementById("select-decryption-key").options;
  let decryptionKey = optionElements[optionElements.selectedIndex].id;
  let decryptedTextElement = document.getElementById("decrypted-text");
  let decryptedText = "";

  for (let i = 0; i < encryptedText.length; i++) {
    let encryptedLetter = encryptedText[i].toLowerCase();
    let indexEncryptedLetter = alphabet.indexOf(encryptedLetter);

    if (!encryptedLetter.match(onlyLettersRegEx)) {
      decryptedText = decryptedText += encryptedLetter;
    } else {
      for (let a = 0; a < decryptionKey; a++) {
        if (indexEncryptedLetter === 25) {
          indexEncryptedLetter = 0;
        } else {
          indexEncryptedLetter++;
        }
      }

      decryptedText = decryptedText += alphabet[indexEncryptedLetter];
    }
  }

  decryptedTextElement.innerHTML = decryptedText;
}

function validateUserInput() {
  let errorMessageElement = document.getElementById("error-message-2");
  let textareaElement = document.getElementById("decryption-textarea");
  let text = textareaElement.value;
  let optionElements = document.getElementById("select-decryption-key").options;
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

  decryptText();
}
</script>

<template>
  <div class="decryption-container">
    <h2>Text verschlüsseln</h2>
    <textarea
      id="decryption-textarea"
      placeholder="Gebe deinen Klartext hier ein..."
    ></textarea>
    <span class="error-message" id="error-message-2"></span>
    <div class="interactive-decryption-elements">
      <button class="decrypt-text" @click="validateUserInput">
        verschlüsseln
      </button>
      <select class="choose-decryption-key" id="select-decryption-key">
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
    <div class="decrypyeted-text-container">
      <h2>Entschlüsselter Text</h2>
      <span class="decrypted-text" id="decrypted-text"
        >Es wurde noch kein Text entschlüsselt</span
      >
    </div>
  </div>
</template>

<style scoped></style>
