<template>
  <section>
    <div class="container">
      <ul class="partners-box d-flx">
        <li v-for="(item, index) in patnersArray" :key="`img-${index}`">
          <a :href="item.site">
            <img :src="item.url" alt="" />
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "Partners",
  data() {
    return {
      patnersArray: [
        {
          url: require("@/assets/img/h1-clients-img-4.png"),
          site: "/",
        },
        {
          url: require("@/assets/img/h1-clients-img-3.png"),
          site: "/",
        },
        {
          url: require("@/assets/img/h1-clients-img-1.png"),
          site: "/",
        },
        {
          url: require("@/assets/img/h1-clients-img-2.png"),
          site: "/",
        },
        {
          url: require("@/assets/img/h1-clients-img-5.png"),
          site: "/",
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
  padding: 8px 0;
  background-color: $bg-7;
  .container {
    .partners-box {
      padding: 3.8rem 3.5rem;
      li {
        img {
          width: 100%;
        }
      }
    }
  }
}
</style>
