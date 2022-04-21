
<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <button @click="count++">{{ count }}</button>
  <HelloWorld msg="Hello World!" />
  <!-- :is="isTimeToSayBye ? HelloWorld : GoogBye" -->
</template>

<script setup lang="ts">
import { ref, watchEffect } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import GoodBye from "./components/GoogBye.vue";

const count = ref(0);
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
