<template>
  <label class="rdm-switch">
    <input type="checkbox" v-model="isChecked" class="rdm-no-size-hide" />
    <span class="rdm-switch-slider"></span>
  </label>
</template>

<script setup>
const isChecked = defineModel();
</script>
