<template>
  <div class="natours">
    <Header />
    <!-- <grid-test /> -->
    <main>
      <About />
      <Features />
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
// import GridTest from "@/components/GridTest.vue";
import About from "@/components/About.vue";
import Features from "@/components/Features.vue";

export default {
  name: "natours",
  components: {
    Header,
    // GridTest,
    Features,
    About
  }
};
</script>

<style lang="scss" scoped></style>
