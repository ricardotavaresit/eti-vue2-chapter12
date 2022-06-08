<template>
  <div id="app">
    <button v-on:click.prevent="show = !show">Show</button>
    <transition name="test">
      <div v-if="show">Presenting...</div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      show: false,
    };
  },
};
</script>

<style>
.test-enter-active,
.test-leave-active {
  transition: opacity 1.5s;
}

.test-enter,
.test-leave-to {
  opacity: 0;
}
</style>
