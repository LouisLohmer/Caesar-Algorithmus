<script setup></script>

<template>
  <div class="text-column">
    <h2>Was ist der Caesar-Algorithmus?</h2>
    <p>
      Der Caesar-Algorithmus ist nach Julius Caesar benannt und eine der
      ältesten bekannten Verschlüsselungsmethoden. Er gehört zur Familie der
      monoalphabetischen Substitutionen und verschlüsselt den Text, indem jeder
      Buchstabe des Klartexts um eine feste Anzahl von Stellen im Alphabet
      verschoben wird.
    </p>
    <ol>
      <li>
        <b>Klartext übergeben:</b> Der ursprungliche Klartext wird
        entgegengenommen, zum Beispiel "Geheimnis"
      </li>
      <li>
        <b>Schlüssel festlegen:</b> Es muss eine Zahl festgelegt werden, welche
        amgibt, um wie viel die einzelnen Buchstaben im Alphabet verschoben
        werden. Dies kann zum Beipiel <b>3</b> sein.
      </li>
      <li>
        <b>Klartext verschlüsslen:</b> Jeder Buchstabe wird um den festgelegten
        Schlüssel im Alphabet verschoben und zu einem Text zusammengesetzt. Zum
        Beispiel wird aus <b>"Geheimnis"</b> dann <b>"JHKKHLPLV"</b>.
      </li>
      <li>
        <b>Verschlüsselten Text entschlüsslen:</b> Beim Entschlüsseln wird der
        verschlüsselte Text um denselben Schlüssel nach links im Alphabet
        verschoben, um den Originaltext zurückzugewinnen. Zum Beispiel wird aus
        <b>"JHKKHLPLV"</b> dann wieder <b>"Geheimnis"</b>.
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

ol li::marker {
  color: var(--royalblue);
}

ol li {
  padding-bottom: 20px;
}
</style>
