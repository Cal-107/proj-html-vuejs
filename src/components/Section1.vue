<template>
  <section class="card-container">
    <ul class="d-flx">
      <li v-for="(item, index) in imgArray1" :key="`img-${index}`">
        <Card1 :url="item.url" />
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 85 85"
          class="qodef-eye eye"
        >
          <circle cx="42.5" cy="42.5" r="42.5" />
          <path
            d="M57.3 43.2c-.2.3-.4.6-.8 1-.3.4-.9 1-1.9 2-.9.9-1.9 1.7-3 2.4s-2.4 1.3-4.1 1.9c-1.7.6-3.3.8-5.1.8-5.5 0-10.5-2.7-14.8-8-.3-.5-.3-1 0-1.5.2-.3.4-.6.8-1 .3-.4.9-1 1.9-2 .9-.9 1.9-1.7 3-2.4s2.4-1.3 4.1-1.9c1.7-.6 3.3-.8 5.1-.8 1.7 0 3.4.3 5.1.8 1.7.6 3 1.2 4.1 1.9 1.1.7 2.1 1.5 3 2.4.9.9 1.6 1.6 1.9 2 .3.4.6.7.8 1 .2.5.2.9-.1 1.4zm-2.7-.7c-.7-.9-1.5-1.7-2.4-2.5-.9-.8-2.3-1.6-4.1-2.5-1.8-.9-3.7-1.3-5.6-1.3-1.9 0-3.8.4-5.6 1.3-1.8.8-3.2 1.7-4.1 2.5-.9.8-1.7 1.6-2.4 2.5.7.9 1.5 1.7 2.4 2.5.9.8 2.3 1.6 4.1 2.5 1.8.9 3.7 1.3 5.6 1.3 4.6-.1 8.6-2.2 12.1-6.3zm-7.8-3.2c.9 1.2 1.2 2.6 1 4-.2 1.5-.9 2.7-2.1 3.6-1.1.7-2.2 1.1-3.3 1.1h-.7c-1.5-.2-2.7-.9-3.6-2.1-.9-1.2-1.2-2.5-1-4 .2-1.5.9-2.6 2.1-3.5 1.2-.9 2.6-1.3 4-1.1 1.5.1 2.7.8 3.6 2zm-.9 3.7c.1-1-.1-1.8-.6-2.6-.5-.7-1.3-1.2-2.3-1.3-.9-.2-1.8 0-2.5.6-.7.5-1.2 1.3-1.3 2.3-.1 1 .1 1.8.6 2.6.5.7 1.3 1.2 2.3 1.3.9.2 1.8 0 2.5-.6s1.1-1.3 1.3-2.3zm-3.3-2.4c-.3.2-.4.5-.4.9s.1.7.4.9c.2.2.5.4.9.4s.7-.1.9-.4c.3-.3.4-.6.4-.9 0-.3-.1-.6-.4-.9-.3-.3-.6-.4-.9-.4s-.7.1-.9.4z"
          />
        </svg>
        <i class="fas fa-eye"></i>
      </li>
    </ul>
  </section>
</template>

<script>
import Card1 from "@/components/Card1.vue";

export default {
  name: "Section1",
  components: {
    Card1,
  },
  data() {
    return {
      imgArray1: [
        {
          url: require("@/assets/img/h3-img-1.jpg"),
        },
        {
          url: require("@/assets/img/h3-img-2.jpg"),
        },
        {
          url: require("@/assets/img/h3-img-3.jpg"),
        },
        {
          url: require("@/assets/img/h3-img-4.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";

.card-container {
  padding: 8px 0;
  ul {
    justify-content: space-between;
    li {
      position: relative;
      width: calc(98.5% / 4);
      background-image: url(../assets/img/13972.jpg);
      background-size: contain;
      cursor: pointer;
      .fa-eye {
        color: $text-color-1;
        font-size: 1.5rem;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        opacity: 0;
        transition: opacity 0.5s ease;
      }
      svg {
        fill: $fill-color-4;
        width: 18%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        opacity: 0;
        transition: opacity 0.5s ease;
      }
      img {
        width: 100%;
        height: 100%;
        opacity: 1;
        transition: opacity 0.5s ease;
      }
      &:hover .eye,
      &:hover .fa-eye {
        opacity: 1;
      }
      &:hover img {
        opacity: 0;
      }
    }
  }
}
</style>
