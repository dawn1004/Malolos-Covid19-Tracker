<template>
  <div id="front">
    <img :src="mySVG" class="background" />
    <img :src="mySVG2" class="background2" />

    <div class="main">
      <div class="left">
        <h1>MALOLOS COVID-19</h1>
        <h2>TRACKER</h2>
        <v-btn color="#00a1ab" dark font-size="136px" large width="160px">Download</v-btn>

        <p
          class="P-on-mobile"
        >Malolos Covid-19 Tracker is a mobile application that will help you to be notified and be upated in current casses of covid-19 virus here in malolos bulacan.</p>
      </div>

      <div class="right">
        <Illustration class="illu" />
      </div>
    </div>
  </div>
</template>

<script>
import Illustration from "./illustration";

export default {
  name: "Front",
  components: {
    Illustration
  },
  data() {
    return {
      mySVG: require("../assets/background.svg"),
      mySVG2: require("../assets/background2.svg")
    };
  }
};
</script>

<style scoped>
.P-on-mobile {
  color: #414141;
  padding-top: 20px;
  font-size: 18px;
  text-align: justify;
}
#front {
  height: 100vh;
  width: 100vw;
  position: relative;
}
.main {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  align-items: center;
}
.background {
  position: absolute;
  top: 0;
  width: 100vw;
  /* height: fit-content; */
}
.background2 {
  position: absolute;
  top: 0;
  width: 100vw;
  /* height: fit-content; */
  display: none;
}
.main .left {
  width: 700px;
}
.main .left h1 {
  color: #f6eedf;
  font-size: 65px;
}
.main .left h2 {
  color: #00263b;
  font-size: 48px;
}

@media only screen and (max-width: 800px) {
  .main {
    flex-direction: column;
    align-items: flex-start;
  }
  .main .left {
    width: 100%;
  }
  .main .left h1 {
    font-size: 40px;
  }
}

@media only screen and (max-width: 500px) {
  .main .left h1 {
    font-size: 28px;
  }
  .main .left h2 {
    font-size: 22px;
    margin-bottom: 10px;
  }
  .main .left {
    width: 100vw;
    /* background: khaki; */
    margin-left: 50px;
  }

  .main .right {
    margin-left: 50px;
  }

  .main {
    top: 90px;
    left: 50%;
    transform: translate(-50%);
  }
  .background2 {
    display: inline;
  }
  .illu {
    display: none;
  }
  .P-on-mobile {
    padding-right: 60px;
  }
}
</style>