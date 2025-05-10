<script setup></script>

<template>
  <div class="encryption-container">
    <h2>Text entschlüsseln</h2>
    <textarea
      placeholder="Gebe deinen verschlüsselten Text hier ein..."
    ></textarea>
    <div class="interactive-encryption-elements">
      <button class="encrypt-text">entschlüsseln</button>
      <select class="choose-encryption-key">
        <option>Wähle einen Schlüssel aus!</option>
        <option>3</option>
        <option>4</option>
        <option>5</option>
        <option>6</option>
        <option>7</option>
        <option>8</option>
        <option>9</option>
        <option>10</option>
        <option>11</option>
        <option>12</option>
        <option>13</option>
        <option>14</option>
        <option>15</option>
        <option>16</option>
        <option>17</option>
        <option>18</option>
        <option>19</option>
        <option>19</option>
        <option>20</option>
        <option>21</option>
        <option>22</option>
        <option>23</option>
        <option>24</option>
        <option>25</option>
      </select>
    </div>
    <div class="encrypyeted-text-container">
      <h2>Entschlüsselter Text</h2>
      <span class="encrypted-text">Es wurde noch kein Text entschlüsselt!</span>
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
</style>
