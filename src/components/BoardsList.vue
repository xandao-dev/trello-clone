<script setup lang="ts">
import { reactive } from "vue";

const data = reactive({
  boards: [
    {
      id: 0,
      img: "https://picsum.photos/id/0/1280/720",
      title: "TailwindCSS",
    },
    {
      id: 1,
      img: "https://picsum.photos/id/1/1280/720",
      title: "VueJS",
    },
    {
      id: 2,
      img: "https://picsum.photos/id/2/1280/720",
      title: "WebXR",
    },
  ]
})

const addRandomBoard = () => {
  console.log("click")
  const randomBoard = {
    id: data.boards.length,
    img: `https://picsum.photos/id/${data.boards.length}/1280/720`,
    title: "Board Novo"
  }
  data.boards.push(randomBoard);
}

</script>
<template>
  <h2 class="text-2xl font-bold py-10">Boards</h2>
  <div
    class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 justify-start gap-8"
  >
    <board-card
      v-for="board in data.boards"
      :key="board.id"
      :img="board.img"
      :title="board.title"
    ></board-card>
    <button class="block" @click="addRandomBoard">New Board +</button>
  </div>
</template>
