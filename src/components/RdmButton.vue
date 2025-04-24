<template>
  <button class="rdm-button">
    <slot v-if="hasSlot"></slot>
    <span v-else>{{ text }}</span>
  </button>
</template>

<script setup>

import { useSlots } from 'vue'

const props = defineProps({
  text: {
    type: String,
    default: ''
  }
})
// check if any slots is provided
const slots = useSlots()
const hasSlot = slots.default

</script>

