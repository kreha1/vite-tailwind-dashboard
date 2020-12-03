<template>
  <h3 class="text-gray-700 text-3xl font-medium">Servers</h3>
  <div class="flex flex-wrap mt-4">
    <server-card />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ServerCard from "../components/desm/ServerCard.vue";

export default defineComponent({
  name: "ServerMonitor",
  components: {
    ServerCard
  }
})

</script>
