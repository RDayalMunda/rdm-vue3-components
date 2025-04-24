<template>
  <div style="display: flex; gap: 10px">
    <div style="display: flex; flex-direction: column; gap: 10px">
      <RdmSwitch v-model="largeSwitch" size="lg" />
      <span>Large switch</span>
    </div>
    <div style="display: flex; flex-direction: column; gap: 10px">
      <RdmSwitch v-model="normalSwitch" />
      <span>Normal switch</span>
    </div>
    <div style="display: flex; flex-direction: column; gap: 10px">
      <RdmSwitch v-model="smallSwitch" size="sm" />
      <span>Small switch</span>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import RdmSwitch from "./RdmSwitch.vue";
const normalSwitch = ref(false);
const largeSwitch = ref(false);
const smallSwitch = ref(false);
</script>
