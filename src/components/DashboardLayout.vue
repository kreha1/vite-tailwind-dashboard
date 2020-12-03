<template>
  <div class="flex h-screen bg-gray-200 font-roboto">
    <sidebar />

    <div class="flex-1 flex flex-col overflow-hidden">
      <the-header />

      <main class="flex-1 overflow-x-hidden overflow-y-auto bg-gray-200">
        <div class="container mx-auto px-6 py-8">
          <slot />
        </div>
      </main>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

import Sidebar from "./Sidebar.vue";
import TheHeader from "./Header.vue";

export default defineComponent({
  components: {
    TheHeader,
    Sidebar,
  },
});
</script>
