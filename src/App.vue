<template>
  <div v-for="(item, idx) in sampleArray" :key="idx">
    <h1>
      {{ item }}
    </h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleArray: ["a", "b", "c", "d", "e", "f", "g"],
    };
  },
};
</script>

<style lang="scss" scoped></style>
