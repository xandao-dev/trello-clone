<template>
	<h2 class="px-10 pt-10 text-2xl font-bold text-gray-800 dark:text-white lg:text-3xl">Boards</h2>
	<div class="grid-cols-fill grid gap-4 px-10 pt-10">
		<board-card v-for="board in data.boards" :key="board.id" :img="board.img" :title="board.title"></board-card>
		<button class="block text-left text-gray-800 dark:text-white" @click="addRandomBoard">New Board +</button>
	</div>
</template>

<script setup lang="ts">
	import { reactive } from 'vue';

	const data = reactive({
		boards: [
			{
				id: 0,
				img: 'https://picsum.photos/id/0/1280/720',
				title: 'TailwindCSS',
			},
			{
				id: 1,
				img: 'https://picsum.photos/id/1/1280/720',
				title: 'VueJS',
			},
			{
				id: 2,
				img: 'https://picsum.photos/id/2/1280/720',
				title: 'WebXR',
			},
		],
	});

	const addRandomBoard = () => {
		const randomBoard = {
			id: data.boards.length,
			img: `https://picsum.photos/id/${data.boards.length}/1280/720`,
			title: 'Board Novo',
		};
		data.boards.push(randomBoard);
	};
</script>

<style scoped>
	.grid-cols-fill {
		grid-template-columns: repeat(auto-fill, minmax(min(270px, 100%), 1fr));
	}
</style>
