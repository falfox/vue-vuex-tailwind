<template>
  <div>
    <div class="flex items-center justify-center font-semibold text-2xl py-10">
      <button
        @click="decrement"
        class="mx-4 px-4 py-1 flex items-center justify-center bg-gray-700 text-white rounded-lg select-none focus:outline-none focus:shadow-outline"
      >
        -
      </button>
      <div
        class="mx-4 w-16 h-16 flex items-center justify-center bg-red-500 rounded-lg text-white"
      >
        {{ count }}
      </div>
      <button
        @click="increment"
        class="mx-4 px-4 py-1 flex items-center justify-center bg-gray-700 text-white rounded-lg select-none focus:outline-none focus:shadow-outline"
      >
        +
      </button>
    </div>
    <div>
        <div class="max-w-2xl mx-auto px-5 py-4 leading-relaxed rounded bg-white shadow">
            <p>
                This is a Vue CLI template with <span class="block-text">TailwindCSS</span> and <span class="block-text">Vuex</span> configured, 
                Vuex uses namespacing and automatically import modules in <span class="block-text">src/store/modules</span> folder.
                This application includes simple counter app using Vuex store.
            </p>
        </div>
    </div>
  </div>
</template>

<script>
import { createNamespacedHelpers } from "vuex";
const { mapState, mapActions } = createNamespacedHelpers("counter");

export default {
  computed: {
    ...mapState(["count"])
  },
  methods: {
    ...mapActions(["increment", "decrement"])
  }
};
</script>

<style>
.block-text {
    @apply bg-gray-300 inline-block px-2 font-light rounded my-1;
}
</style>