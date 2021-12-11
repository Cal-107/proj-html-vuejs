<template>
  <section>
    <section class="card-container">
      <ul class="d-flx">
        <li v-for="(item, index) in imgArray2" :key="`img-${index}`">
          <Card1 :url="item.url" />
        </li>
      </ul>
    </section>
  </section>
</template>

<script>
import Card1 from "@/components/Card1.vue";

export default {
  name: "OurTeam",
  components: {
    Card1,
  },
  data() {
    return {
      imgArray2: [
        {
          url: require("@/assets/img/h1-team-1a-700x700.jpg"),
        },
        {
          url: require("@/assets/img/h1-team-2a.jpg"),
        },
        {
          url: require("@/assets/img/h1-team-4a.jpg"),
        },
        {
          url: require("@/assets/img/h1-team-3a.jpg"),
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
      width: calc(100% / 4);
      background-image: url(../assets/img/13972.jpg);
      background-size: contain;
      cursor: pointer;
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
      &:hover img {
        opacity: 0;
      }
    }
  }
}
</style>
