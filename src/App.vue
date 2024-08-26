<template>
  <div class="wrapper">
    <div v-for="item in otherArray" :key="item.id">
      <h1>{{ item.name }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleArray: ["a", "b", "c", "d", "e", "f", "g"],
      otherArray: [
        {
          id: 0,
          name: "han",
        },
        {
          id: 1,
          name: "eun",
        },
        {
          id: 2,
          name: "beom",
        },
      ],
    };
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
}
</style>
