<template>
  <section>
    <section class="card-container">
      <ul class="d-flx">
        <li v-for="(item, index) in imgArray2" :key="`img-${index}`">
          <Card1 :url="item.url" />
          <div class="hover-effect d-flxCol justContCent alignIteCent">
            <span class="worker upCase"> {{ item.worker }} </span>
            <span class="role"> {{ item.role }} </span>
            <div class="socials">
              <a href="/"><i class="fab fa-instagram"></i></a>
              <a href="/"><i class="fab fa-twitter"></i></a>
              <a href="/"><i class="fab fa-facebook-f"></i></a>
            </div>
          </div>
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
          worker: 'Frank Bailey',
          role: 'Kitchen Porter',
          social1: null,
          social2: null,
          social3: null,
        },
        {
          url: require("@/assets/img/h1-team-2a.jpg"),
          worker: 'Alice Fox',
          role: 'Call Center',
          social1: null,
          social2: null,
          social3: null,
        },
        {
          url: require("@/assets/img/h1-team-4a.jpg"),
          worker: 'Walter White',
          role: 'Chief Chef',
          social1: null,
          social2: null,
          social3: null,
        },
        {
          url: require("@/assets/img/h1-team-3a.jpg"),
          worker: 'Jessie Pinkman',
          role: 'Co-Chef',
          social1: null,
          social2: null,
          social3: null,
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
      .hover-effect {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 85%;
        height: 85%;
        color: $text-color-1;
        background-color: $bg-16;
        opacity: 0;
        transition: all .5s ease .1s;
      }
      .worker {
        font-size: 1.6rem;
      }
      .role {
        font-size: .8rem;
        padding-bottom: .8rem;
      }
      .socials {
        a {
          i{
            padding: 0 .3rem;
          }
        }
      }
      &:hover .hover-effect {
        opacity: 1;
        letter-spacing: .30rem;
      }
      &:hover img {
        opacity: 0;
      }
    }
  }
}
</style>
