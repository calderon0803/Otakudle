<script setup>
import { useGuessCharacterStore } from "@/store/guessCharacterStore.js";

const guessCharacterStore = useGuessCharacterStore();
</script>

<template>
  <div id="character-attempt-header">
    <div>
      <fieldset
        v-if="guessCharacterStore.attempts.length > 0"
        id="attempt"
        class="input-flex-group attempt"
      >
        <div class="header">Personaje</div>
        <div class="header">Gategoría</div>
        <div class="header">Ubicación</div>
        <div class="header">Runas</div>
        <div class="header">Drop</div>
        <div class="header">Salud</div>
      </fieldset>
    </div>
    <div id="character-attempt-list"></div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  color: white;
  text-shadow: 2px 2px 3px #000;
  text-align: center;
  border-bottom: 3px solid white;
  width: 80px;
  margin: 3px;
}
</style>
