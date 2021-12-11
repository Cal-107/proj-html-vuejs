<template>
  <div id="app">
    <!-- Start Header -->
    <Header />

    <!-- Start Main -->
    <main>
      <Section1 />
      <Section2 />
      <PizzeSpecials />
      <BuildYourPizza />
      <OurTeam />
      <Partners />
      <ChoosePizza />
      <PizzaDeals />
      <BookATable />
    </main>

    <!-- Start Footer -->
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Section1 from "@/components/Section1.vue";
import Section2 from "@/components/Section2.vue";
import PizzeSpecials from "@/components/PizzeSpecials.vue";
import BuildYourPizza from "@/components/BuildYourPizza.vue";
import OurTeam from "@/components/OurTeam.vue";
import Partners from "@/components/Partners.vue";
import ChoosePizza from "@/components/ChoosePizza.vue";
import PizzaDeals from "@/components/PizzaDeals.vue";
import BookATable from "@/components/BookATable.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Section1,
    Section2,
    PizzeSpecials,
    BuildYourPizza,
    OurTeam,
    Partners,
    ChoosePizza,
    PizzaDeals,
    BookATable,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/styles/variables";
@import "@/styles/globals";
</style>
