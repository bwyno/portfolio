<template>
  <section id="contact" class="h-screen fourth-section"></section>
</template>
<style>
.fourth-section {
  background-color: rgba(0, 0, 0, 0.7);
  animation: background-black-exit linear forwards;
  animation-timeline: view();
  animation-range: entry;
}

@keyframes background-black-entry {
  from {
    background-color: rgba(0, 0, 0, 0.8);
  }
  to {
    background-color: rgba(0, 0, 0, 0);
  }
}
</style>