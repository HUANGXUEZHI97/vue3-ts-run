
<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld
    msg="Hello Vue 3 + TypeScript + Vite"
    v-model:count="count"
    v-model:userInfo="useInfo"
  />
</template>

<script lang="ts">
import { ref, reactive } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
export default {
  components: {
    HelloWorld,
  },
  setup() {
    const count = ref(0);
    const useInfo = reactive({
      name: "KK",
      age: 2,
    });

    return {
      useInfo,
      count,
    };
  },
};
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
