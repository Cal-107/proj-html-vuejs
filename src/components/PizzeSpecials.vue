<template>
  <section class="d-flx">
    <div class="box">
      <div class="photo-box">
        <img class="img-relative" src="../assets/img/h1-img-4.jpg" alt="" />
        <img class="img-abs" src="../assets/img/h1-img-7n.png" alt="" />
      </div>
    </div>
    <div class="menu-list d-flx justContCent alignIteCent">
      <div class="menu-box">
        <h1 class="title upCase">Specials*</h1>
        <div class="description">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut facere
          consequuntur velit magnam eaque inventore.
        </div>
        <div>
          <h3 class="subTitle upCase">
            <span class="price">$10</span> combo piccolo
          </h3>
          <ul>
            <li class="description2">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vero
              obcaecati ipsum vel impedit odio.
            </li>
          </ul>
        </div>
        <div>
          <h3 class="subTitle upCase">
            <span class="price">$20</span> combo mezzo
          </h3>
          <ul>
            <li class="description2">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vero
              obcaecati ipsum vel impedit odio.
            </li>
          </ul>
        </div>
        <div>
          <h3 class="subTitle upCase">
            <span class="price">$30</span> combo grande
          </h3>
          <ul>
            <li class="description2">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vero
              obcaecati ipsum vel impedit odio.
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PizzeSpecial",
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";

section {
    padding: .5rem 0;
  .box,
  .menu-list {
    width: 50%;
  }
  .photo-box {
    width: 100%;
    height: 100%;
    position: relative;
    img {
      width: 100%;
    }
    .img-relative {
      height: 100%;
    }
    .img-abs {
      width: 40%;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
  .menu-list {
    .menu-box {
      width: 60%;
      .title {
        font-size: 2rem;
        font-weight: 500;
      }
      .subTitle {
        font-weight: 400;
        padding-bottom: .2rem;
      }
      .price {
        font-weight: 400;
        color: $text-color-13;
        padding-right: 0.5rem;
      }
      .description {
        padding: 0.1rem 0 2rem;
      }
      .description,
      .description2 {
        font-weight: 400;
        width: 76%;
        color: $text-color-4;
        letter-spacing: 0.04rem;
      }
      ul {
        li {
          padding-left: 2.5rem;
          font-size: 0.9rem;
          padding-bottom: 1.2rem;
        }
      }
    }
  }
}
</style>
