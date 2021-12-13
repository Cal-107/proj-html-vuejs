<template>
  <footer>
    <section class="d-flx">
      <div class="faq d-flx justContCent alignIteCent">
        <div class="faq-box d-flx">
          <!-- first column -->
          <div class="restaurants">
            <h4 class="upCase">find our restaurants</h4>
            <ul v-for="(restaurant, i) in restourantArray" :key="`id-${i}`">
              <li>{{ restaurant.address }}</li>
              <li>{{ restaurant.city }}</li>
              <li>{{ restaurant.phoneNumber }}</li>
            </ul>
          </div>

          <!-- second column -->
          <div class="working-hours">
            <h4 class="upCase">working hours</h4>
            <ul v-for="(info, i) in infoArray" :key="`id2-${i}`">
              <li class="day upCase">
                {{ info.day }}<span v-show="info.check">*</span>
              </li>
              <li
                :class="{ colorClosed: info.workingHours == 'Kitchen Closed' }"
              >
                {{ info.workingHours }}
              </li>
            </ul>

            <ul class="socials d-flx">
              <h4 class="upCase">Follow Us:</h4>
              <li>
                <a href="/"><i class="fab fa-twitter"></i></a>
              </li>
              <li>
                <a href="/"><i class="fab fa-facebook-f"></i></a>
              </li>
              <li>
                <a href="/"><i class="fab fa-instagram"></i></a>
              </li>
              <li>
                <a href="/"><i class="fab fa-linkedin-in"></i></a>
              </li>
            </ul>
          </div>

          <!-- third column -->
          <div class="quote upCase">
            the don peppe crew <br />
            first and foremost <br />
            values an authentic,<br />
            well baked slice of <br />
            pizza.
          </div>
        </div>

        <!-- natural product image -->
        <a href="">
          <img
            class="natural-product-logo"
            src="../assets/img/footer-bottom-img.png"
            alt=""
          />
        </a>

        <!-- signature -->
        <div class="signature">
          Created with &#9829; by
          <a class="sig-color" href="/">Calogero Bonito</a>
        </div>
      </div>
      <div class="bg-footer"></div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      restourantArray: [
        {
          address: "1614 E. Bell Rd #104.",
          city: "Salerno, AZ 85022",
          phoneNumber: "(602) 867-1010",
        },
        {
          address: "204 E. Pizzetta Tommaso",
          city: "Sorrento, AZ 85022",
          phoneNumber: "(358) 867-1010",
        },
        {
          address: "Vale Puglia 54",
          city: "Torre Del Greco, AZ 85022",
          phoneNumber: "(359) 867-1010",
        },
        {
          address: "Corso Itali AA",
          city: "Naples, AZ 85022",
          phoneNumber: "(989) 867-1010",
        },
      ],
      infoArray: [
        {
          day: "monday",
          workingHours: "Kitchen Closed",
          check: false,
        },
        {
          day: "tuesady until friday",
          workingHours: "9:00 - 22:00",
          check: false,
        },
        {
          day: "saturday",
          workingHours: "Saturday 11am to midnight",
          check: true,
        },
        {
          day: "sunday",
          workingHours: "9:00 - 22:00",
          check: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables";
@import "@/styles/utilities";
footer {
  height: 600px;
  overflow: hidden;
  section {
    height: 100%;
    .faq,
    .bg-footer {
      width: 50%;
    }
    .faq {
      background-image: url(../assets/img/footer-img-2.jpg);
      background-color: $bg-18;
      color: $text-color-1;
      position: relative;
      padding-bottom: 3.5rem;
      h4 {
        color: $text-color-7;
        font-weight: 500;
        letter-spacing: 0.06rem;
      }
      .faq-box {
        justify-content: space-between;
        width: 90%;
        ul {
          padding-top: 1rem;
          font-size: 0.8rem;
          color: $text-color-5;
          font-weight: 300;
          letter-spacing: 0.05rem;
        }
        .working-hours {
          ul {
            li:nth-child(1) {
              font-weight: 400;
              letter-spacing: 0.03rem;
              span {
                color: $text-color-12;
                font-size: 1rem;
                padding-left: 0.2rem;
              }
            }
            .day {
              color: $text-color-7;
            }
          }
          .socials {
            padding-top: 2rem;
            h4 {
              font-weight: 400;
              letter-spacing: 0.03rem;
            }
            i {
              padding: 0 0.3rem;
              font-size: 0.8rem;
              transition: all 0.5s ease;
              &:hover {
                transform: translateY(-5px);
              }
            }
          }
        }
      }
      .quote {
        width: 35%;
        font-size: 1.4rem;
      }

      .natural-product-logo {
        position: absolute;
        right: 5%;
        bottom: 7%;
      }

      .signature {
        position: absolute;
        bottom: 7%;
        left: 5%;
        font-size: 0.8rem;
        color: $text-color-6;
        font-weight: 300;
        letter-spacing: 0.06rem;
        .sig-color {
          color: $text-color-9;
        }
      }
    }
    .bg-footer {
      background-image: url(../assets/img/footer-img-1.jpg);
      background-size: cover;
      background-position: center;
      height: 100%;
    }
  }
}

// binded class
.colorClosed {
  color: $text-color-12;
}
</style>
