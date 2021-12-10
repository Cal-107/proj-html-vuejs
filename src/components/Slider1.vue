<template>
  <div class="slider-container">
    <div class="img-box d-flx justContCent alignIteCent">
      <img class="urban-bg" src="../assets/img/h3-rev-img-5.png" alt="" />
      <img class="img-absolute" src="../assets/img/h3-rev-img-6.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider1",
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";

.slider-container {
  position: relative;
  padding-top: 1rem;
  padding-bottom: 4rem;
  .img-box {
    padding: 1rem 0;
    .urban-bg {
      width: 65%;
    }
    .img-absolute {
      width: 25%;
      position: absolute;
      top: 53%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
}
</style>
