<template>
  <div>
    <h3 class="text-gray-700 text-3xl font-medium">Modal</h3>
    <button
      @click="open = true"
      class="mt-3 px-6 py-3 bg-indigo-600 rounded-md text-white font-medium tracking-wide hover:bg-indigo-500"
    >
      Open Modal
    </button>
    <modal :open="open" title="Your modal">
      <template #default>
        <p>Modal content passed to a slot</p>
      </template>
      <template #footer>
        <button
          @click="open = false"
          class="px-6 py-3 bg-transparent p-3 rounded-lg text-indigo-500 hover:bg-gray-100 hover:text-indigo-400 mr-2"
        >
          Close
        </button>
        <button
          @click="open = false"
          class="px-6 py-3 bg-indigo-600 rounded-md text-white font-medium tracking-wide hover:bg-indigo-500"
        >
          Action
        </button>
      </template>
    </modal>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import Modal from "../components/Modal.vue"

export default defineComponent({
  components: {
    Modal
  },
  setup() {
    const open = ref(false);
    return {
      open,
    };
  },
});
</script>

<style>
.modal {
  transition: opacity 0.25s ease;
}
</style>