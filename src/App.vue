<script setup>
import { ref } from "vue";
import ValidationInput from "./components/ValidationInput.vue";

const val = ref("");
</script>

<template>
  <p>This should only display uppercase vowels and is synced with the input below: {{ val }}</p>
  <ValidationInput v-model="val" />
  <p>If you type a vowel in the input, the output is in sync with the input.</p>
  <p>If you input consonants, the output will correctly display the expected output, but the input will not be updated properly.</p>
  <p>Its model in the JS still seems to be correct, since the label comes back down as if it was empty, even if it isn't.</p>
  <p>The culprit is the FloatLabel component. Without that, it works fine.</p>
</template>
