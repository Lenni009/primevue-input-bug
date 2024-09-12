<script setup>
import { watchEffect } from "vue";
import BaseInput from "./BaseInput.vue";

const model = defineModel({ type: String, required: true });

const vowels = "AEIOU";

watchEffect(
  () =>
    (model.value = model.value
      .toUpperCase()
      .split("")
      .filter((char) => vowels.includes(char))
      .join(""))
);
</script>

<template>
  <BaseInput v-model="model" />
</template>
