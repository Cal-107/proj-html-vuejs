<template>
  <section>
    <Testimonial />
    <PrevNextBtn />
  </section>
</template>

<script>
import Testimonial from "@/components/Testimonial.vue";
import PrevNextBtn from "@/components/PrevNextBtn.vue";

export default {
  components: {
    Testimonial,
    PrevNextBtn,
  },
  name: "Section2",
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";
section {
    overflow: hidden;
    position: relative;
    background-color: #f6f7f2;
    background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
    background-size: 95%;
    background-position-x: -20px;
    background-position-y: 10px;
    background-repeat: no-repeat;
    height: 400px;
}
</style>
