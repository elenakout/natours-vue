<template>
  <div class="natours">
    <navigation />
    <Header />
    <!-- <grid-test /> -->
    <main>
      <About />
      <Features />
      <tours />
      <stories />
      <booking />
    </main>
    <Footer />
    <popup />
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
import Footer from "@/components/Footer.vue";
import Navigation from "@/components/Navigation.vue";
import Popup from "@/components/Popup.vue";

export default {
  name: "natours",
  components: {
    Header,
    // GridTest,
    Features,
    About,
    Tours,
    Stories,
    Booking,
    Footer,
    Navigation,
    Popup
  }
};
</script>

<style lang="scss" scoped></style>
