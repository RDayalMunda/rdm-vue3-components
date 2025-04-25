<template>
  <h2>Start here</h2>
  <div class="rdm-accordion" :class="{ 'rdm-accordion-open': isOpen }">
    <div
      class="rdm-accordion-header"
      ref="accordionHeader"
      @click="toggleAccordion"
    >
      Header : {{ headerHeight }} {{ contentHeight }}
    </div>
    <div class="rdm-accordion-content" ref="accordionContent">
      <slot name="content" />
    </div>
  </div>
  <h2>End here</h2>
</template>

<script setup>
import { computed, onMounted, ref } from "vue";

const props = defineProps({
  title: {
    type: String,
  },
  template: {
    type: String,
    default: "content",
  },
  name: {
    type: String,
  },
});

const toggle = ref(false);
const isOpen = ref(false);

const accordionHeader = ref(null);
const accordionContent = ref(null);
const headerHeight = ref(0);
const contentHeight = ref(0);

const accordionHeight = computed(() => {
  return isOpen.value
    ? headerHeight.value + contentHeight.value
    : headerHeight.value;
});
const accordionHeightInPx = computed(() => {
  return accordionHeight.value + "px";
});

function toggleAccordion() {
  if (!props.name) {
    isOpen.value = !isOpen.value;
  } else {
    console.log("handle cases for accordion name", props.name);
  }
}

function handleResize() {
  headerHeight.value = accordionHeader.value.offsetHeight;
  contentHeight.value = accordionContent.value.offsetHeight;
}

onMounted(() => {
  const observer = new ResizeObserver(handleResize);
  observer.observe(accordionHeader.value);
  observer.observe(accordionContent.value);
});
</script>
<style>
.rdm-accordion {
  height: v-bind(accordionHeightInPx);
}
</style>
