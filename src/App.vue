<template>
  <div id="app">
    <Section1 />
    <!-- <div class="white"></div> -->
    <Standing />
    <Table />
    <Footer />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import Section1 from "./components/section1";
import Table from "./components/table";
import Standing from "./components/standing";
import Footer from "./components/footer";

export default {
  name: "App",
  components: {
    Section1,
    Table,
    Standing,
    Footer
  },
  data() {
    return {};
  }
};
</script>

<style >
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: roboto;
}

body,
html {
  height: 100%;
  margin: 0;
}

body {
  background: url("./assets/background3.svg");
  background-size: cover;
  background-repeat: no-repeat;
}

.white {
  height: 100vh;
  width: 100vw;
  background-color: white;
  position: absolute;
  top: 0;
  animation-name: white-animate;
  animation-duration: 1s;
  opacity: 1;
  left: 100vw;
}

@keyframes white-animate {
  from {
    left: 0;
  }
  to {
    left: -100vw;
  }
}
@media only screen and (max-width: 1150px) {
  body {
    background-size: auto;
  }
}

@media only screen and (max-width: 500px) {
  body {
    background: url("./assets/mobile-view.png");
    background-repeat: no-repeat;
    overflow: hidden;
    background-size: 100vw 100vh;
  }
}
</style>
