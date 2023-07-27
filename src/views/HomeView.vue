<script setup lang="ts">
</script>

<template>
  <div id="HomeView">
    <h1>This is the home view page</h1>
  </div>
</template>

<style lang="scss" scoped>
#HomeView {
  width: 100vw;
  height: 100vh;
  background-color: lightgreen;
  @extend .center;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
