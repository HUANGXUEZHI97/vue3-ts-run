<template>
  <h1 v-bind="$attrs" ref="h1">{{ msg }}</h1>

  <button type="button" @click="addCount">count is: {{ count }}</button>
  <div>{{ userInfo.name }}</div>
</template>

<script  lang="ts">
export default {
  props: ["count", "userInfo", "msg"],
  // emits: ["update:count"],
  setup(props, {}) {},
  methods: {
    addCount() {
      this.$emit("update:count", this.count + 1);
    },
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
