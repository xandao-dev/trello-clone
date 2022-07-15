<template>
  <div
    v-if="isSideBarOpen"
    class="h-full p-3 space-y-2 w-60 bg-gray-50 text-gray-800"
  >
    <div class="flex items-center p-2 space-x-4">
      <img
        src="data:image/jpeg;base64,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"
        alt="user profile image"
        class="w-12 h-12 rounded-full bg-gray-500"
      />
      <div>
        <h2 class="text-lg font-semibold">Orange Lemur</h2>
        <span class="flex items-center space-x-1">
          <a
            rel="noopener noreferrer"
            href="#"
            class="text-xs hover:underline text-gray-600"
            >View profile</a
          >
        </span>
      </div>
    </div>
    <div class="divide-y divide-gray-300">
      <ul class="pt-2 pb-4 space-y-1 text-sm">
        <li class="bg-gray-100 text-gray-900">
          <a
            rel="noopener noreferrer"
            href="#"
            class="flex items-center p-2 space-x-3 rounded-md"
          >
            <span class="material-symbols-rounded">grid_view</span>
            <span>Boards</span>
          </a>
        </li>
        <li>
          <a
            rel="noopener noreferrer"
            href="#"
            class="flex items-center p-2 space-x-3 rounded-md"
          >
            <span class="material-symbols-rounded">create_new_folder</span>
            <span>Templates</span>
          </a>
        </li>
        <li>
          <a
            rel="noopener noreferrer"
            href="#"
            class="flex items-center p-2 space-x-3 rounded-md"
          >
            <span class="material-symbols-rounded">settings</span>
            <span>Settings</span>
          </a>
        </li>
      </ul>
      <ul class="pt-4 pb-2 space-y-1 text-sm">
        <li>
          <a
            @click="setSidebarOpen(!isSideBarOpen)"
            rel="noopener noreferrer"
            href="#"
            class="flex items-center p-2 space-x-3 rounded-md"
          >
            <span class="material-symbols-rounded"
              >keyboard_double_arrow_left</span
            >
            <span>Collapse</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
  <div v-else>
    <button @click="setSidebarOpen(!isSideBarOpen)" class="rounded-full m-5">
      <span class="material-symbols-rounded">menu</span>
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const isSideBarOpen = ref(true);

const setSidebarOpen = (value: boolean) => {
  isSideBarOpen.value = value;
};
</script>
