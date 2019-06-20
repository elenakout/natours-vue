<template>
  <div class="natours">
    <Header />
    <grid-test />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import GridTest from "@/components/GridTest.vue";

export default {
  name: "natours",
  components: {
    Header,
    GridTest
  }
};
</script>

<style lang="scss" scoped></style>
