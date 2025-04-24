<template>
  <div>
    <button @click="handleClick">Click me</button>
    <button @click="handleClick">👌</button>
    <button @click="handleClick">A simple button with a long text</button>
  </div>
  <hr />
  <div>
    <RdmButton text="Click Me" @click="handleClick" />
  </div>
</template>

<script setup>
import RdmButton from "./RdmButton.vue";

function handleClick() {
  console.log("clicked");
}
</script>
