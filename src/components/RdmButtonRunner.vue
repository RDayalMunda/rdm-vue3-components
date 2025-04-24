<template>
  <div>
    <button>Click me</button>
    <button>👌</button>
    <button>A simple button with a long text</button>
  </div>
  <hr />
  <div>
    <RdmButton text="Click Me" />
    <RdmButton>
      👌
    </RdmButton>
    <RdmButton>A simple button with a long text</RdmButton>
  </div>
</template>

<script setup>
import RdmButton from './RdmButton.vue'
</script>
