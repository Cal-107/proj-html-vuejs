<template>
  <div class="testimonial-container upCase d-flx justContCent">
    <div class="text-box d-flxCol justContCent alignIteCent">
      <h1><i class="fas fa-quote-left"></i></h1>
      <h3>
        "forget the trendy pizza shops, this hidden spot makes the best new
        york-style pizza slice in naples"
      </h3>
      <div>
        washington post 2018
      </div>
      <div class="ellipsis">
        <i class="fas fa-circle"></i>
        <i class="fas fa-circle"></i>
        <i class="fas fa-circle"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Testimonial",
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";

.testimonial-container {
  height: 100%;
  .text-box {
    padding: 1rem 0;
    height: 100%;
    text-align: center;
    width: 36%;
    h3 {
      font-weight: 500;
      padding: 1rem 0 .2rem;
      color: #303030;
      letter-spacing: .05rem;
    }
    div {
      color: $text-color-12;
      font-size: .6rem;
      letter-spacing: .1rem;
    }
    .fa-quote-left {
      font-size: 70px;
      color: $text-color-6;
    }
    .ellipsis {
      padding: 1rem;
      color: $text-color-3;
      font-size: .3rem;
      i {
        padding: .11rem;
      }
      i:nth-child(1) {
        transform: scale(1.4);
        color: $text-color-7;
      }
    }
  }
}
</style>
