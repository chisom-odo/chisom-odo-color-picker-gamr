<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { ref, reactive } from "@vue/reactivity";
import colorManager from "../composables/colorManager";

export default {
  data() {
    return {
      colors: [],
    };
  },
  method: {
    matchColor() {},
  },
  setup() {
    const { colors, matchColor, message } = colorManager();
    return {
      colors,
      matchColor,
      message,
    };
  },
};
</script>

<style></style>
