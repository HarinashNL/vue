<script setup>
import { ref } from "vue";
</script>

<template>
  <main>
    <!-- <div class="container">
      <Transition>
        <h1 v-if="showGreet">HelloWorld</h1>
        <h1 v-else>goodbye</h1>
      </Transition>
    </div>
    <button @click="showGreet = !showGreet">Toggle</button> -->
    <div class="container">
      <input type="text" placeholder="Add person to invite" />
      <ul>
        <li>Selena</li>
        <li>Kevin</li>
      </ul>
    </div>
  </main>
</template>

<style scoped>
/* .fade-enter-from {
  opacity: 0;
}

.fade-enter-to {
  opacity: 1;
}

.fade-enter-active {
  transition: all 0.5s ease;
}

.fade-leave-to {
  opacity: 0;
}

.fade-leave-active {
  transition: all 0.5s ease;
}

.container {
  position: relative;
}

h1 {
  position: absolute;
}

button {
  margin-top: 50px;
} */
.container {
  max-width: 300px;
  margin: 0 auto;
}

.container input {
  width: 100%;
  border-radius: 5px;
  border: 1px solid rgba(128, 128, 128, 0.13);
  padding: 10px;
  margin-bottom: 20px;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.12);
}

ul {
  display: inline;
  list-style: none;
  margin: 0px;
  padding: 0px;
}

li {
  list-style: none;
  width: 300px;
  border-radius: 5px;
  padding: 5px 10px;
  margin-top: 10px;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.12);
  text-align: center;
  cursor: pointer;
}
</style>
