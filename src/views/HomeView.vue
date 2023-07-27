<script setup lang="ts">
import { ref, reactive } from 'vue';

// using reactive ====================
// const state = reactive({
//   name: 'Johnny', // will automatically inferred to be a string
//   age: 25 as number | string
// })
// const changeName = (newName: string) => state.name = newName
// const changeAge = (newAge: number | string) => state.age = newAge

// using refs ====================
const name = ref('Johnny Chang')
const age = ref<number | string>(26)

const changeName = (newName: string) => name.value = newName
const changeAge = (newAge: number | string) => age.value = newAge

</script>

<template>
  <div id="HomeView">
    <!-- ========== using reactive ========== -->

    <!-- <h1>{{ state.name }} -- {{ state.age }}</h1>
    <button @click="changeName('Joby')">Change Name</button>
    <button @click="changeAge(30)">Change Age</button> -->

    <!-- ========== using refs ========== -->
    <h1>{{ name }} -- {{ age }}</h1>
    <button @click="changeName('Hello world')">Ref Change Name</button>
    <button @click="changeAge('123')">Ref Change Age</button>

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
