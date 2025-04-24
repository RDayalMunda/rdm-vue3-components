<template>
  <label class="rdm-switch" :size="size">
    <input type="checkbox" v-model="isChecked" class="rdm-no-size-hide" />
    <span class="rdm-switch-slider"></span>
  </label>
</template>

<script setup>
const isChecked = defineModel();

const props = defineProps({
  size: {
    type: String,
    default: "md",
  },
});
</script>
