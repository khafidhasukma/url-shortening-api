<template>
  <div class="overflow-hidden">
    <!-- banner -->
    <section id="banner">
      <div class="container">
        <div class="row d-flex align-items-center">
          <div class="col-12 col-md-6">
            <h1 class="fw-700 title">
              More than just <br />
              shorter links
            </h1>
            <p class="desc fw-500 my-3 lh">Build your brand’s recognition and get detailed insights on how your links are performing.</p>
            <button class="btn-started rounded-pill border-0 fw-700">Get Started</button>
          </div>
          <div class="col-12 col-md-6">
            <img src="/assets/img/illustration-working.svg" alt="" />
          </div>
        </div>
      </div>
    </section>
    <!-- end banner -->

    <!-- shorten link -->
    <div class="container">
      <section id="shorten">
        <div class="input d-flex gap-2 justify-content-center">
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
        <div class="row row-cols-3">
          <div v-for="(value, key) in statistics" :key="key" class="col contents">
            <div class="ms-4 icon rounded-circle">
              <img :src="value.image" height="40" alt="" />
            </div>
            <div class="bg-white py-5 px-4 statistics rounded">
              <h5 class="fw-700 mb-3">{{ value.title }}</h5>
              <p class="text-secondary lh">{{ value.desc }}</p>
            </div>
          </div>
        </div>
        <hr class="hr-content" />
      </div>
    </section>
    <!-- end statistics -->

    <!-- boost -->
    <section id="boost">
      <h1 class="text-white fw-700 mb-4">Boost your links today</h1>
      <button class="btn-started rounded-pill border-0 fw-700">Get Started</button>
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
