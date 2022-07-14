<script setup lang="ts">
defineProps({
  img: { type: String, required: true },
  title: { type: String, required: true },
});
</script>
<template>
  <div class="relative flex flex-wrap justify-center">
    <div
      class="relative max-w-sm min-w-[340px] bg-white shadow-md rounded-3xl p-2 mx-1 my-3 cursor-pointer"
    >
      <div class="overflow-x-hidden rounded-2xl relative">
        <img class="h-40 rounded-2xl w-full object-cover" :src="img" />
      </div>
      <div class="mt-4 pl-2 mb-2 flex justify-around">
        <div>
          <p
            class="text-lg font-semibold text-gray-900 mb-0"
            v-text="title"
          ></p>
        </div>
      </div>
    </div>
  </div>
</template>
