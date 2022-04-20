<template>
  <h1 v-bind="$attrs">Hello {{ msg }}</h1>
  <slot name="name"></slot>
</template>

<script lang="ts" setup>
defineProps({
  msg: String,
});
console.log("hello script setup");

defineExpose({
  age: 18,
});
</script>
<script lang="ts">
export default {
  created() {
    console.log("created");
  },
  beforeCreate() {
    console.log("beforeCreate");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    console.log("mounted");
  },
};
</script>


<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
