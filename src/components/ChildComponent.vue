<template>
  <div>{{ props1 }}</div>
  <div>{{ props2 }}</div>
  <div>{{ props3.id }}</div>
  <div>{{ props3.name }}</div>
</template>

<script setup lang="ts">
// 동일하게 setup과 lang 설정

import { toRefs } from "vue";

interface Obj {
  id: number;
  name: string;
}

interface Props {
  props1: String;
  props2: Number;
  props3: Obj;
}

const props = defineProps<Props>(); // 방법1. defineProps 내장함수 사용
const { props1, props2, props3 } = toRefs(props); // 방법2. 구조분해 할당으로 받아올 경우 toRefs 내장함수 사용 import 해야함!!
</script>

<style lang="scss" scoped></style>
