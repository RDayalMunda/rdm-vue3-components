<template>
  <RdmAccordion title="Accordion Title" template="content">
    <template #content>
      <button @click="isShow = !isShow">Show/Hide</button>
      <p>Accordion Body</p>
      <p>Accordion Body 1</p>
      <p>Accordion Body 2</p>
      <p v-if="isShow">Hidable Accordion Body</p>
      <p>Accordion Body 4</p>
      <p>Accordion Body 5</p>
    </template>
  </RdmAccordion>
  <h2>Accordion End care</h2>
</template>

<script setup>
import { ref } from "vue";
import RdmAccordion from "./RdmAccordion.vue";

const isShow = ref(false);
</script>
