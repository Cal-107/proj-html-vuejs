<template>
  <section class="d-flx justContCent alignIteCent">
    <div class="box upCase d-flx alignIteCent">
      <div>
        <input type="text" placeholder="1 Person" />
        <i class="fas fa-user-friends"></i>
      </div>
      <span>for</span>
      <div>
        <input type="text" placeholder="11/29/2020" />
        <i class="far fa-calendar"></i>
      </div>
      <span>at</span>
      <div>
        <input type="text" placeholder="7:00 pm" />
        <i class="far fa-clock"></i>
      </div>
      <span></span>
      <button class="btn-custom upCase">book a table</button>
      <div class="sponsor">
        *Powered by <a href="https://www.opentable.com/">OpenTable</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BookATable",
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";

section {
  margin: 8px 0;
  background-image: url(../assets/img/h3-background-img-3.jpg);
  background-size: cover;
  color: $text-color-1;
  .box {
    padding: 5rem;
    position: relative;
    span {
      width: 50px;
      text-align: center;
      font-size: 0.85rem;
    }
    input {
      padding: 1rem 5rem 0.8rem 1rem;
      border: 2px solid $border-color-6;
      transition: border-radius 0.5s ease;
      font-size: 0.8rem;
      color: $text-color-5;
      &:focus {
        outline: none;
        border-radius: 40px;
      }
    }
    div {
      position: relative;
      i {
        position: absolute;
        right: 7%;
        top: 38%;
        color: $text-color-6;
        font-size: 0.8rem;
      }
    }
    .sponsor {
      font-size: 0.7rem;
      font-weight: 300;
      letter-spacing: 0.04rem;
      text-transform: none;
      position: absolute;
      bottom: 26%;
    }
    .btn-custom {
      padding: 1.2rem 4rem;
      font-size: 0.55rem;
    }
    .sponsor {
      &:hover a {
        text-decoration: underline;
      }
    }
  }
}
</style>
