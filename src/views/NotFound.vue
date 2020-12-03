<template>
  <div>
    <h3 class="text-gray-700 text-3xl font-medium">Not found</h3>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

interface User {
  name: string;
  email: string;
  title: string;
  title2: string;
  status: string;
  role: string;
}

export default defineComponent({
  setup() {
    const testUser: User = {
      name: "John Doe",
      email: "john@example.com",
      title: "Software Engineer",
      title2: "Web dev",
      status: "Active",
      role: "Owner",
    };

    const users = ref<User[]>([...Array(10).keys()].map(() => testUser));

    return {
      users,
    };
  },
});
</script>
