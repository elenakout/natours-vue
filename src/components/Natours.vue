<template>
  <div class="natours">
    <Header />
    <!-- <grid-test /> -->
    <main>
      <About />
      <Features />
      <tours />
      <stories />
      <booking />
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
// import GridTest from "@/components/GridTest.vue";
import About from "@/components/About.vue";
import Features from "@/components/Features.vue";
import Tours from "@/components/Tours.vue";
import Stories from "@/components/Stories.vue";
import Booking from "@/components/Booking.vue";

export default {
  name: "natours",
  components: {
    Header,
    // GridTest,
    Features,
    About,
    Tours,
    Stories,
    Booking
  }
};
</script>

<style lang="scss" scoped></style>
