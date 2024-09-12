<script setup>
import InputText from "primevue/inputtext";
import FloatLabel from "primevue/floatlabel";

const model = defineModel({ type: String, required: true });
</script>

<template>
  <div>Comment out this div in src/components/BaseInput.vue and see the bug disappear in dev (but not in prod)</div>
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
