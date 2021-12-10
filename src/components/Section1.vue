<template>
  <section class="card-container">
    <ul class="d-flx">
      <li v-for="(item, index) in imgArray1" :key="`img-${index}`">
        <Card1 :url="item.url" />
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
      width: calc(98.5% / 4);
      img {
        width: 100%;
      }
    }
  }
}
</style>
