<template>
  <section>
    <div class="container">
      <div class="quote upCase d-flx alignIteCent">
        <p>
          go ahead and <br />
          build your <br />
          own pizza <br />
          we won't <br />
          judge!
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BuildYourPizza",
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";
section {
  height: 500px;
  background-image: url(../assets/img/h3-background-img.jpg);
  background-attachment: fixed;
  .container {
    height: 100%;
  }
  .quote {
    padding-left: 3rem;
    width: 50%;
    height: 100%;
    font-size: 3rem;
    font-weight: 500;
    line-height: 55px;
    color: $text-color-1;
  }
}
</style>
