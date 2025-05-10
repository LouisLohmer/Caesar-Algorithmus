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
  let encryptedTextMessage = "";
  let textarea = document.getElementById("encryption-textarea");
  let decryptedTextMessage = textarea.value.split("");
  let options = document.getElementById("select-encryption-key").options;
  let encryptionKey = options[options.selectedIndex].id;
  let encryptedTextElement = document.getElementById("encrypted-text");
  let indexEncryptedLetter;

  for (let i = 0; i < decryptedTextMessage.length; i++) {
    let indexDecryptedLetter = alphabet.indexOf(
      decryptedTextMessage[i].toLowerCase()
    );

    for (let a = 0; a < encryptionKey; a++) {
      // Bei Verschlüsseln: indexDecryptedLetter === 25, indexDecryptedLetter = 0;,indexDecryptedLetter++;
      if (indexDecryptedLetter === 0) {
        indexDecryptedLetter = 25;
      } else {
        indexDecryptedLetter--;
      }
    }

    encryptedTextMessage = encryptedTextMessage +=
      alphabet[indexDecryptedLetter];
  }

  encryptedTextElement.innerHTML = encryptedTextMessage;
}

function validateUserInput() {
  const onlyLettersRegEx = /^[a-zA-Z]+$/;
  let errorMessageTextElement = document.getElementById("error-message");
  let textarea = document.getElementById("encryption-textarea");
  let textMessage = textarea.value;
  let splittedTextMessage = textarea.value.split("");
  let options = document.getElementById("select-encryption-key").options;
  let selectedOptionId = options[options.selectedIndex].id;

  if (textMessage.length === 0) {
    errorMessageTextElement.innerHTML = "Das Textfeld darf nicht leer sein!";
    return;
  } else {
    errorMessageTextElement.innerHTML = "";
  }

  for (let i = 0; i < splittedTextMessage.length; i++) {
    if (!splittedTextMessage[i].match(onlyLettersRegEx)) {
      errorMessageTextElement.innerHTML =
        "Das Textfeld darf nur Buchstaben enthalten!";
      return;
    }
  }

  if (selectedOptionId === "null") {
    errorMessageTextElement.innerHTML =
      "Wähle bitte einen validen Schlüssel aus!";
  } else {
    errorMessageTextElement.innerHTML = "";
  }

  encryptText();
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
      <span class="encrypted-text" id="encrypted-text"
        >Es wurde noch kein Text entschlüsselt</span
      >
    </div>
  </div>
</template>

<style scoped>
h2 {
  color: var(--imperial-gold);
}

.encryption-container,
.encrypyeted-text-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}

.encrypt-text {
  background-color: var(--royalblue);
  color: var(--marble-white);
  font-size: var(--text-font);
}

.encrypt-text:hover {
  color: var(--imperial-gold);
}

.interactive-encryption-elements {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding-bottom: 50px;
}

.choose-encryption-key {
  height: 34px;
  border-radius: 5px;
  background-color: var(--royalblue);
  color: var(--marble-white);
}

.encrypted-text {
  padding-top: 20px;
}

.error-message {
  color: var(--red);
  padding-bottom: 20px;
}
</style>
