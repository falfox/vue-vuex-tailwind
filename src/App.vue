<template>
  <div id="app">
    <h1 class="mt-12 font-semibold text-gray-800 text-2xl text-center">
      Vue + Vuex + TailwindCSS<br/>Starter Template
    </h1>
    <Introduction></Introduction>
  </div>
</template>

<script>
import Introduction from "./components/Introduction.vue";

export default {
  name: "app",
  components: {
    Introduction
  }
};
</script>

<style>
body {
  @apply font-sans antialiased bg-gray-200;
}
</style>
