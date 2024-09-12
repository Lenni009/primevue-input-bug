<script setup>
import InputText from "primevue/inputtext";
import FloatLabel from "primevue/floatlabel";

const model = defineModel({ type: String, required: true });
</script>

<template>
  <!--The FloatLabel is bugged. Comment it out and see everything working as expected-->
  <FloatLabel class="label-combo">
    <InputText v-model="model" id="input" type="text" />
    <label for="input">This is a label</label>
  </FloatLabel>
</template>

<style>
.label-combo {
  border: 1px solid black;
  padding: 0.25rem;
  border-radius: 6px;
  margin-block-start: 2rem;
}
</style>
