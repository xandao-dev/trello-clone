<script setup lang="ts">
defineProps({
  img: { type: String, required: true },
  title: { type: String, required: true },
});
</script>
<template>
  <div class="bg-white shadow-md rounded-xl p-2">
    <div class="aspect-w-16 aspect-h-9">
      <img class="rounded-xl" :src="img" />
    </div>
    <div class="mt-4 pl-2 mb-2 flex justify-around">
      <p class="text-lg font-semibold text-gray-900 mb-0" v-text="title"></p>
    </div>
  </div>
</template>
