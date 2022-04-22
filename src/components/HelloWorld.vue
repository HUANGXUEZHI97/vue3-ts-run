<template>
  <h1 v-bind="$attrs">Hello {{ msg }}</h1>
  <h2>{{ name }}</h2>
  <h2>{{ useinfo.name }}</h2>
  <h2>{{ data.name }}</h2>
  <ul>
    <li v-for="hb in data.hobby" :key="hb">
      {{ hb }}
    </li>
  </ul>
  <button @click="say">{{ name }}</button>
</template>

<script lang="ts" setup>
import { ref, reactive } from "vue";
defineProps({
  msg: String,
});
defineExpose({
  age: 18,
});

let name = ref<string | number>("燕儿");
let age = ref(18);
let useinfo = ref({
  name: "kk",
  age: 2,
});
let date = reactive(/\s/);
let data = reactive({
  name: "燕儿",
  age: 18,
  job: {
    occupation: "程序员",
    salary: "10k",
  },
  hobby: ["刷剧", "吃鸡", "睡觉"],
});
console.log(date);
console.log(name);
console.log(useinfo);
console.log(data);
//方法
function say() {
  name.value = 123;
  useinfo.value.name = "金刚";
  data.name = "小李子";
  data.hobby[0] = "学习";
  date = 123;
}
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
