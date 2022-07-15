<template>
  <div class="grid-template h-full">
    <side-bar class="template-side-bar" />
    <div class="template-app max-w-screen-xl mx-auto w-full overflow-y-auto">
      <h1 class="text-center text-4xl font-bold text-orange-500 py-10">
        Vue.js Forge - Orange Lemur
      </h1>
      <boards-grid></boards-grid>
    </div>
  </div>
</template>

<style scoped>
.grid-template {
  display: grid;
  grid-template-columns: min-content auto;
  grid-template-rows: 1fr;
  grid-template-areas: "side-bar app";
}

.grid-template > .template-side-bar {
  grid-area: side-bar;
}

.grid-template > .template-app {
  grid-area: app;
}
</style>
