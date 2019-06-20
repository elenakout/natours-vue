<template>
  <div class="natours">
    <Header />
    <!-- <grid-test /> -->
    <main>
      <About />
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
// import GridTest from "@/components/GridTest.vue";
import About from "@/components/About.vue";

export default {
  name: "natours",
  components: {
    Header,
    // GridTest,
    About
  }
};
</script>

<style lang="scss" scoped></style>
