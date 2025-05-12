<script setup></script>

<template>
  <div class="text-column">
    <h2>Was ist der Caesar-Algorithmus?</h2>
    <p class="typewriter-animaton">
      Der Caesar-Algorithmus ist nach Julius Caesar benannt und eine der
      ältesten bekannten Verschlüsselungsmethoden. Er gehört zur Familie der
      monoalphabetischen Substitutionen und verschlüsselt den Text, indem jeder
      Buchstabe des Klartexts um eine feste Anzahl von Stellen im Alphabet
      verschoben wird.
    </p>
    <ol>
      <li class="typewriter-animaton">
        <b>Klartext übergeben:</b> Der ursprungliche Klartext wird
        entgegengenommen, zum Beispiel "Geheimnis"
      </li>
      <li class="typewriter-animaton">
        <b>Schlüssel festlegen:</b> Es muss eine Zahl festgelegt werden, welche
        amgibt, um wie viel die einzelnen Buchstaben im Alphabet verschoben
        werden. Dies kann zum Beipiel <b>3</b> sein.
      </li>
      <li class="typewriter-animaton">
        <b>Klartext verschlüsslen:</b> Jeder Buchstabe wird um den festgelegten
        Schlüssel im Alphabet verschoben und zu einem Text zusammengesetzt. Zum
        Beispiel wird aus <b>"Geheimnis"</b> dann <b>"JHKHLPqLV"</b>.
      </li>
      <li class="typewriter-animaton">
        <b>Verschlüsselten Text entschlüsslen:</b> Beim Entschlüsseln wird der
        verschlüsselte Text um denselben Schlüssel nach links im Alphabet
        verschoben, um den Originaltext zurückzugewinnen. Zum Beispiel wird aus
        <b>"JHKHLPqLV"</b> dann wieder <b class="blink-caret-animation">"Geheimnis"</b>
      </li>
    </ol>
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
  letter-spacing: .15em;
  animation: 
    typing 3.5s steps(40, end)
}

.blink-caret-animation {
  border-right: .15em solid var(--imperial-gold); 
  animation: 
    blink-caret .75s step-end infinite;
}

ol li::marker {
  color: var(--royalblue);
}

ol li {
  padding-bottom: 20px;
}

/* The typing effect */
@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: orange; }
}
</style>
