<template>
  <div>
    <button @click="handleClick">Click me</button>
    <button @click="handleClick">👌</button>
    <button @click="handleClick">A simple button with a long text</button>
  </div>
  <hr />
  <div class="custom-container">
    <div>
      <label>Primary Button</label>
      <RdmButton text="Click Me" @click="handleClick" />
    </div>
    <div>
      <label>Secondary Button</label>
      <RdmButton text="Click Me" variant="secondary" @click="handleClick" />
    </div>
  </div>
</template>

<script setup>
import RdmButton from "./RdmButton.vue";

function handleClick() {
  console.log("clicked");
}
</script>
<style scoped>
.custom-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.custom-container label {
  margin: 10px;
}
</style>
