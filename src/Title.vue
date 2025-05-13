<script setup lang="ts">
import { ref, watch } from "vue";
import { animate } from "animejs";

const show = ref(true);

watch(show, (newVal) => {
  animate("#title", {
    opacity: newVal ? 1 : 0,
    duration: 1000,
    easing: "easeInOutSine",
  });
});
</script>

<template>
  <div>
    <h1 id="title">Hello World</h1>
    <button @click="show = !show">{{ show ? "hide" : "show" }}</button>
  </div>
</template>
