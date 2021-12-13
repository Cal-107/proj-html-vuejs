<template>
  <section>
    <div class="d-flxCol justContCent alignIteCent">
      <!-- title section -->
      <div class="title">
        <div class="sub-title upCase">choose your flavour</div>
        <h1 class="upCase">the best pizza menu in town</h1>
        <p class="description">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eum
          doloremque odit, vero deleniti perferendis assumenda libero voluptas.
        </p>
      </div>
    </div>

    <!-- pizzas section -->
    <ul class="d-flx">
      <li class="upCase" v-for="(pizza, i) in pizzasArray" :key="`pizza-${i}`">
        <img :src="pizza.url" alt="" />
        <h4>{{ pizza.name }}</h4>
        <span v-show="pizza.priceDeleted" class="priceDeleted"> $65.00 </span>
        <span class="price1">{{ pizza.price }}</span>
        <div v-show="pizza.soldOut" class="sold-out">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 85 85"
            class="qodef-eye"
          >
            <circle cx="42.5" cy="42.5" r="42.5" />
            <path
              d="M57.3 43.2c-.2.3-.4.6-.8 1-.3.4-.9 1-1.9 2-.9.9-1.9 1.7-3 2.4s-2.4 1.3-4.1 1.9c-1.7.6-3.3.8-5.1.8-5.5 0-10.5-2.7-14.8-8-.3-.5-.3-1 0-1.5.2-.3.4-.6.8-1 .3-.4.9-1 1.9-2 .9-.9 1.9-1.7 3-2.4s2.4-1.3 4.1-1.9c1.7-.6 3.3-.8 5.1-.8 1.7 0 3.4.3 5.1.8 1.7.6 3 1.2 4.1 1.9 1.1.7 2.1 1.5 3 2.4.9.9 1.6 1.6 1.9 2 .3.4.6.7.8 1 .2.5.2.9-.1 1.4zm-2.7-.7c-.7-.9-1.5-1.7-2.4-2.5-.9-.8-2.3-1.6-4.1-2.5-1.8-.9-3.7-1.3-5.6-1.3-1.9 0-3.8.4-5.6 1.3-1.8.8-3.2 1.7-4.1 2.5-.9.8-1.7 1.6-2.4 2.5.7.9 1.5 1.7 2.4 2.5.9.8 2.3 1.6 4.1 2.5 1.8.9 3.7 1.3 5.6 1.3 4.6-.1 8.6-2.2 12.1-6.3zm-7.8-3.2c.9 1.2 1.2 2.6 1 4-.2 1.5-.9 2.7-2.1 3.6-1.1.7-2.2 1.1-3.3 1.1h-.7c-1.5-.2-2.7-.9-3.6-2.1-.9-1.2-1.2-2.5-1-4 .2-1.5.9-2.6 2.1-3.5 1.2-.9 2.6-1.3 4-1.1 1.5.1 2.7.8 3.6 2zm-.9 3.7c.1-1-.1-1.8-.6-2.6-.5-.7-1.3-1.2-2.3-1.3-.9-.2-1.8 0-2.5.6-.7.5-1.2 1.3-1.3 2.3-.1 1 .1 1.8.6 2.6.5.7 1.3 1.2 2.3 1.3.9.2 1.8 0 2.5-.6s1.1-1.3 1.3-2.3zm-3.3-2.4c-.3.2-.4.5-.4.9s.1.7.4.9c.2.2.5.4.9.4s.7-.1.9-.4c.3-.3.4-.6.4-.9 0-.3-.1-.6-.4-.9-.3-.3-.6-.4-.9-.4s-.7.1-.9.4z"
            />
          </svg>
          <span>SOLD</span>
        </div>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "ChoosePizza",
  data() {
    return {
      pizzasArray: [
        {
          url: require("@/assets/img/h3-product-img-1a-100x100.png"),
          name: "bismark",
          price: "$55.00",
          priceDeleted: true,
          soldOut: false,
        },
        {
          url: require("@/assets/img/h3-product-img-2a-150x150.png"),
          name: "fiori di zucca",
          price: "$7.00 - $55.00",
          soldOut: false,
        },
        {
          url: require("@/assets/img/h3-product-img-3a-150x150.png"),
          name: "valdostana",
          price: "$55.00",
          soldOut: true,
        },
        {
          url: require("@/assets/img/h3-product-img-4a-150x150.png"),
          name: "pizza tartufata",
          price: "$45.00",
          soldOut: false,
        },
        {
          url: require("@/assets/img/h3-product-img-5a-150x150.png"),
          name: "francescana",
          price: "$25.00",
          soldOut: false,
        },
        {
          url: require("@/assets/img/h3-product-img-6a-100x100.png"),
          name: "campagnola",
          price: "$55.00 - $95.00",
          soldOut: false,
        },
        {
          url: require("@/assets/img/h3-product-img-5a-150x150.png"),
          name: "lello",
          price: "$55.00",
          soldOut: false,
        },
        {
          url: require("@/assets/img/h3-product-img-6a-100x100.png"),
          name: "deliziosa",
          price: "$55.00",
          soldOut: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";

section {
  padding-bottom: 5rem;
  .title {
    text-align: center;
    width: 24%;
    padding: 4.5rem 0 2rem;
    .sub-title {
      font-weight: 400;
      font-size: 0.65rem;
      letter-spacing: 0.08rem;
      word-spacing: 0.1rem;
      color: $text-color-12;
    }
    h1 {
      font-weight: 500;
      font-size: 1.7rem;
      padding: 0.1rem 0 0.7rem;
    }
    .description {
      color: $text-color-5;
      font-weight: 300;
    }
  }

  ul {
    overflow: scroll;
    letter-spacing: 0.03rem;
    line-height: 21px;
    position: relative;
    h4 {
      color: $text-color-6;
      font-weight: 400;
      font-size: 0.9rem;
      padding-top: 0.7rem;
    }
    .price1 {
      color: $text-color-12;
      font-size: 0.85rem;
    }
    .priceDeleted {
      text-decoration: line-through;
      font-size: 0.85rem;
      color: $text-color-4;
      padding-right: 0.5rem;
    }
    li {
      text-align: center;
      padding: 3rem;
      position: relative;
      transition: all 0.5s ease;
      &:hover {
        transform: translateY(-20px);
      }
      img {
        width: 200px;
        cursor: pointer;
      }
    }
    .sold-out {
      svg {
        fill: $fill-color-4;
        width: 50px;
        top: 14%;
        right: 18%;
      }
      span {
        color: $text-color-1;
        font-size: 0.7rem;
        top: 18%;
        right: 22.5%;
      }
      svg,
      span {
        position: absolute;
      }
    }
  }
}
</style>
