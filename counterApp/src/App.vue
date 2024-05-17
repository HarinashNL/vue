<template>
  <main>
    <div>
      <h4>The current count</h4>
      <h1>{{ count }}</h1>
      <button @click="addToCount()">+</button>
      <button @click="subToCount()">-</button>
    </div>
  </main>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0);

const addToCount = () => {
  count.value = count.value + 1;
};

const subToCount = () => {
  count.value = count.value - 1;
};
</script>

<style scoped>
main {
  background-color: aliceblue;
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
}

h1,
h4 {
  color: black;
}

div {
  text-align: center;
}
</style>
