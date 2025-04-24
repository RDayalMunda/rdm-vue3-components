<template>
  <RdmToggle v-model="isDarkTheme" />
  dark-theme ->{{ isDarkTheme }}
  <h1>Hello World</h1>
  <RdmButtonRunner />
</template>

<script setup>
import RdmButtonRunner from "./components/RdmButtonRunner.vue";
import RdmToggle from "./components/RdmSwitch.vue";
import "./scss/_variables.scss";
import "./scss/_styles.scss";
import { ref, watch } from "vue";

const isDarkTheme = ref(document.body.classList.contains("rdm-dark"));
watch(isDarkTheme, (newVal) => {
  if (newVal) {
    document.body.classList.add("rdm-dark");
  } else {
    document.body.classList.remove("rdm-dark");
  }
});
</script>
