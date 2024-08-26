<template>
  <div>
    <ChildComponent :props1="title" :props2="createAt" :props3="obj" />
  </div>
</template>

<script setup lang="ts">
//setup 선언
import { reactive, ref } from "vue"; //import
import ChildComponent from "./components/ChildComponent.vue";

interface Obj {
  id: number;
  name: string;
}

const title = ref<string>("APP에서 생성된 데이터"); //ref를 통해 state 선언
const createAt = ref<number>(2024);
const obj = reactive<Obj>({ id: 2024, name: "한은범" }); // !!객체는 ref보단 reactive를 사용하는 것을 권장!!
</script>

<style lang="scss" scoped></style>
