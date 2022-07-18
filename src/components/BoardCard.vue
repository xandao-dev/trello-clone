<script setup lang="ts">
	defineProps({
		img: { type: String, required: true },
		title: { type: String, required: true },
	});
</script>
<template>
	<div class="rounded-xl bg-white p-2 shadow-md">
		<div class="aspect-w-16 aspect-h-9">
			<img class="rounded-xl" :src="img" />
		</div>
		<div class="mt-4 mb-2 flex justify-around pl-2">
			<p class="mb-0 text-lg font-semibold text-gray-900" v-text="title"></p>
		</div>
	</div>
</template>
