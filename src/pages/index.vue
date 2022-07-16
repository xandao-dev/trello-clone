<template>
  <div class="grid-template h-full">
    <side-bar class="template-side-bar" />
    <nav-bar class="template-nav-bar"></nav-bar>
    <main class="template-app max-w-screen-xl mx-auto w-full overflow-y-auto">
      <boards-grid></boards-grid>
    </main>
  </div>
</template>

<style scoped>
.grid-template {
  display: grid;
  grid-template-columns: min-content auto;
  grid-template-rows: min-content auto;
  grid-template-areas:
    "nav-bar nav-bar"
    "side-bar app";
}

.grid-template > .template-side-bar {
  grid-area: side-bar;
}

.grid-template > .template-nav-bar {
  grid-area: nav-bar;
}

.grid-template > .template-app {
  grid-area: app;
}
</style>
