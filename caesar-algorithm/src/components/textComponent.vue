<script setup></script>

<template>
  <div class="text-column">
    <h2>Was ist der Caesar-Algorithmus?</h2>
    <p id="animated-element">
      Der Caesar-Algorithmus ist nach Julius Caesar benannt und eine der
      ältesten bekannten Verschlüsselungsmethoden. Er verschlüsselt den Text,
      indem jeder Buchstabe des Klartexts um eine feste Anzahl von Stellen im
      Alphabet verschoben wird.
    </p>
    <ul>
      <li id="animated-element-2">
        <b>1. Klartext übergeben:</b> Der ursprungliche Klartext wird
        entgegengenommen, zum Beispiel "Geheimnis"
      </li>
      <li id="animated-element-3">
        <b>2. Schlüssel festlegen:</b> Es muss eine Zahl festgelegt werden,
        welche amgibt, um wie viel die einzelnen Buchstaben im Alphabet
        verschoben werden. Dies kann zum Beipiel <b>3</b> sein.
      </li>
      <li id="animated-element-4">
        <b>3. Klartext verschlüsslen:</b> Jeder Buchstabe wird um den
        festgelegten Schlüssel im Alphabet nach rechts verschoben und zum
        verschlüsselten Text zusammengesetzt. Zum Beispiel wird aus
        <b>"Geheimnis"</b> dann <b>"JHKHLPqLV"</b>.
      </li>
      <li id="animated-element-5">
        <b>4. Verschlüsselten Text entschlüsslen:</b> Jeder Buchstabe wird um
        den festgelegten Schlüssel im Alphabet nach rechts verschoben und zum
        Klartext zusammengesetzt. Zum Beispiel wird aus <b>"JHKHLPqLV"</b> dann
        wieder
        <b id="animated-element-6">"Geheimnis"</b>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.text-column {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 15px 25px 15px 25px;
}

.typewriter-animaton {
  overflow: hidden;
  white-space: nowrap;
  margin: 0 auto;
  letter-spacing: 0.15em;
  animation: typing 3.5s steps(40, end);
}

.blink-caret-animation {
  border-right: 0.15em solid var(--imperial-gold);
  animation: blink-caret 0.75s step-end infinite;
}

ul li {
  padding-bottom: 20px;
}

ul {
  list-style: none;
}

/* The typing effect */
@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from,
  to {
    border-color: transparent;
  }
  50% {
    border-color: orange;
  }
}
</style>
