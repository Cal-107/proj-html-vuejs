<template>
  <section class="d-flx upCase">
    <div class="box d-flx justContCent alignIteCent">
      <!-- left side -->
      <div class="info-box">
        <div class="slogan">made with love</div>
        <h1 class="title">delish pizza deals</h1>
        <div
          class="info d-flx"
          v-for="(event, i) in eventsArray"
          :key="`event-${i}`"
        >
          <div class="date">
            <div class="day">{{ event.day }}</div>
            <div class="month">{{ event.month }}</div>
          </div>
          <div class="event">
            <div class="type">
              {{ event.event }}
            </div>
            <div class="place d-flx alignIteCent">
              <i class="fas fa-map-marker-alt"></i> {{ event.place }}
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- rigth side -->
    <div class="comic-bg">
      <img src="../assets/img/h3-img-5a.jpg" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  name: "PizzaDeals",
  data() {
    return {
      eventsArray: [
        {
          day: "02",
          month: "nov",
          event: "traditional neapolitan pies in kyoto pizza mercato",
          place: "204 e. pizzetta tommaso",
        },
        {
          day: "03",
          month: "nov",
          event: "terarazza patio dining space opening this weekend",
          place: "204 e. pizzetta tommaso",
        },
        {
          day: "05",
          month: "nov",
          event: "sienna private dining room with stéphane brunn",
          place: "204 e. pizzetta tommaso",
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
  .box {
    color: $text-color-1;
    width: 50%;
    background-color: $bg-18;
    background-image: url(../assets/svg/grunge-pattern-01.svg);
    .info-box {
      width: 47%;
      margin-right: 5rem;
      .slogan {
        color: $text-color-13;
        font-size: 0.65rem;
        letter-spacing: 0.07rem;
      }
      .title {
        padding-top: 0.5rem;
        font-size: 1.7rem;
        font-weight: 500;
      }
      .info {
        border-bottom: 1.5px dotted $text-color-6;
        padding: 2rem 0;
        &:last-child {
          border: none;
          padding-bottom: 0;
        }
        .date {
          padding-right: 2rem;
          line-height: 36px;
          text-align: center;
          .day {
            font-size: 2.4rem;
            font-weight: 600;
            color: $text-color-13;
          }
          .month {
            font-size: 1.3rem;
          }
        }
        .type {
          font-size: 1.3rem;
          line-height: 28px;
          padding-bottom: 0.7rem;
        }
        .place {
          color: $text-color-13;
          font-size: 0.6rem;
          text-transform: capitalize;
          letter-spacing: 0.07rem;
          i {
            font-size: 0.8rem;
            padding-right: 0.5rem;
          }
        }
      }
    }
  }
  .comic-bg {
    width: 50%;
    img {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
