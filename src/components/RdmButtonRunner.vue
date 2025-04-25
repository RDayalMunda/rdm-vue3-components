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
      <RdmButton class="m-2" text="Click Me" @click="handleClick" />
      <RdmButton
        class="m-2"
        @click="handleClick"
        variant="primary-outline"
        text="Click Me"
      />
    </div>
    <div class="">
      <label>Disabled Primary Button</label>
      <RdmButton class="m-2" disabled @click="handleClick" text="Click Me" />
      <RdmButton
        class="m-2"
        disabled
        @click="handleClick"
        text="Click Me"
        variant="primary-outline"
      />
    </div>
    <div class="">
      <label>Secondary Button</label>
      <RdmButton
        class="m-2"
        text="Click Me"
        variant="secondary"
        @click="handleClick"
      />
      <RdmButton
        class="m-2"
        text="Click Me"
        variant="secondary-outline"
        @click="handleClick"
      />
    </div>
    <div>
      <label>Disabled Secondary Button</label>
      <RdmButton
        class="m-2"
        text="Click Me"
        disabled
        variant="secondary"
        @click="handleClick"
      />
      <RdmButton
        class="m-2"
        text="Click Me"
        disabled
        variant="secondary-outline"
        @click="handleClick"
      />
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
.custom-container-item {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.m-2 {
  margin: 6px;
}
</style>
