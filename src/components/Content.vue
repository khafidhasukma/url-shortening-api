<template>
  <div class="overflow-hidden">
    <!-- banner -->
    <section id="banner">
      <div class="container">
        <div class="row d-flex align-items-center">
          <div class="col-12 col-md-6 text-center text-md-start px-3 px-md-0">
            <h1 class="fw-700 title">
              More than just <br />
              shorter links
            </h1>
            <p class="desc fw-500 my-3 lh">Build your brand’s recognition and get detailed insights on how your links are performing.</p>
            <div class="mt-4">
              <a href="#shorten" class="btn-started rounded-pill border-0 fw-700">Get Started</a>
            </div>
          </div>
          <div class="col-12 col-md-6 order-first order-md-last text-center text-md-start">
            <img src="/assets/img/illustration-working.svg" class="ilustration-img" alt="" />
          </div>
        </div>
      </div>
    </section>
    <!-- end banner -->

    <!-- shorten link -->
    <div class="container">
      <section id="shorten">
        <div class="input d-flex flex-column flex-md-row gap-2 justify-content-center">
          <input type="text" class="form-control" placeholder="Shorten a link here..." />
          <button class="btn-started rounded-3 border-0 fw-700">Shorten It!</button>
        </div>
      </section>
    </div>
    <!-- end shorten link -->

    <!-- statistics -->
    <section id="statistics">
      <div class="container">
        <div class="text-center mb-4">
          <h1 class="fw-700 mb-3">Advanced Statistics</h1>
          <div class="d-flex justify-content-center">
            <p class="w-50 text-secondary desc lh">Track how your links are performing across the web with our advanced statistics dashboard.</p>
          </div>
        </div>
        <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3">
          <div v-for="(value, key) in statistics" :key="key" class="col contents text-center text-md-start">
            <div class="ms-md-4 icon mx-auto rounded-circle">
              <img :src="value.image" height="40" alt="" />
            </div>
            <div class="bg-white py-5 px-4 statistics rounded">
              <h5 class="fw-700 mb-3">{{ value.title }}</h5>
              <p class="text-secondary lh">{{ value.desc }}</p>
            </div>
          </div>
        </div>
        <hr class="hr-content d-none d-md-block" />
        <div class="vl d-sm-none"></div>
      </div>
    </section>
    <!-- end statistics -->

    <!-- boost -->
    <section id="boost">
      <h1 class="text-white fw-700 mb-4">Boost your links today</h1>
      <a href="#shorten" class="btn-started rounded-pill border-0 fw-700">Get Started</a>
    </section>
    <!-- end boost -->
  </div>
</template>

<style scoped>
#banner {
  height: 100vh;
}
.title {
  font-size: 3.5rem;
}
.btn-started {
  padding: 0.75rem 2rem;
  color: white;
  background: var(--cyan);
}
.btn-started:hover {
  background: var(--cyan2);
}
.desc {
  color: var(--gray);
  font-size: 18px;
}
#shorten {
  background-color: var(--very-dark-violet);
  background-image: url("/assets/img/bg-shorten-desktop.svg");
  border-radius: 12px;
  padding: 2rem;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.input {
  width: 100% !important;
  border-radius: 12px;
}
input {
  background-color: white;
  padding: 1rem;
  border: none;
  outline: none;
}
.form-control:focus {
  box-shadow: none !important;
}
.form-control {
  width: 80% !important;
}

#statistics {
  margin-top: -55px;
  background: var(--gray2);
  padding: 8rem 0;
}
.icon {
  padding: 1rem;
  background: var(--very-dark-blue);
  width: 75px;
  display: flex;
  justify-content: center;
  align-content: center;
  position: relative;
}
.statistics {
  margin-top: -30px;
  height: 17rem;
}
.contents:nth-child(2) {
  margin-top: 4rem;
}
.contents:nth-child(3) {
  margin-top: 8rem;
}
#boost {
  background-color: var(--very-dark-violet);
  background-image: url("/assets/img/bg-boost-desktop.svg");
  padding: 4rem 0;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  background-repeat: no-repeat;
  background-size: cover;
}
hr {
  margin-top: -15rem;
  margin-bottom: 15rem;
  opacity: 1 !important;
}
hr.hr-content {
  border: 5px solid var(--cyan);
}
.lh {
  line-height: 2rem !important;
}

@media only screen and (max-width: 991.98px) {
  .statistics {
    height: auto;
  }
  .title {
    font-size: 2.5rem !important;
  }
  .desc {
    font-size: 1rem;
  }
  h5 {
    font-size: 1.125rem;
  }
  p {
    font-size: 0.875rem;
  }
  h1 {
    font-size: 1.5rem;
  }
}
@media only screen and (max-width: 767.98px) {
  #banner {
    height: max-content;
  }
  .ilustration-img {
    width: 450px;
    margin-bottom: 1rem;
  }

  #shorten {
    margin-top: 8rem !important;
  }
  .form-control {
    width: 100% !important;
  }
  .contents:nth-child(3) {
    margin-top: 2rem;
  }
  .contents:nth-child(2) {
    margin-top: 0;
  }
  .w-50 {
    width: 100% !important;
  }
  #statistics {
    padding: 8rem 1rem;
    margin-top: -90px;
  }
  .statistics {
    height: auto;
  }

  .vl {
    border-left: 6px solid var(--cyan);
    height: 50rem;
    position: absolute;
    margin-top: -55rem !important;
    right: 50%;
  }
  .contents {
    position: relative;
    z-index: 1;
  }
}
@media only screen and (max-width: 575.98px) {
  .contents:nth-child(3) {
    margin-top: 4rem;
  }
  .contents:nth-child(2) {
    margin-top: 4rem;
  }
}
</style>

<script>
export default {
  data() {
    return {
      statistics: [
        {
          image: "/assets/img/icon-brand-recognition.svg",
          title: "Brand Recognition",
          desc: "Boost your brand recognition with each click. Generic links don’t mean a thing. Branded links help instil confidence in your content.",
        },
        {
          image: "/assets/img/icon-detailed-records.svg",
          title: "Detailed Records",
          desc: " Gain insights into who is clicking your links. Knowing when and where people engage with your content helps inform better decisions.",
        },
        {
          image: "/assets/img/icon-fully-customizable.svg",
          title: "Fully Customizable",
          desc: "Improve brand awareness and content discoverability through customizable links, supercharging audience engagement.",
        },
      ],
    };
  },
};
</script>
