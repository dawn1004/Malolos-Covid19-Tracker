<template>
  <div id="sectio1">
    <div class="nav">
      <img class="logo" src="../assets/malolosLogo.png" alt />
      <a class="title" href="#">MALOLOS INFORMATION</a>
    </div>

    <div class="heading">
      <h1>MALOLOS COVID-19</h1>
      <h2>TACKER</h2>
      <!-- <button>Download</button> -->
      <v-btn color="#FF5D6C" dark font-size="136px" large width="160px">Download</v-btn>
    </div>

    <img class="viruses virus-1" src="../assets/virus.svg" alt />
    <img class="viruses virus-2" src="../assets/virus.svg" alt />
    <img class="viruses virus-3" src="../assets/virus.svg" alt />
  </div>
</template>

<script>
export default {
  name: "Section1"
};
</script>


<style scoped>
#sectio1 {
  height: 100vh;
}
.nav {
  display: flex;
  align-items: center;
  margin: 10px 0px 0px 90px;
}
.logo {
  width: 50px;
  height: 50px;
  margin-right: 12px;
}
.title {
  text-decoration: none;
  font-size: 24px;
  font-weight: 500;
  color: #353535;
  letter-spacing: 1.5px;
}
.heading {
  margin-left: 140px;
  margin-top: 100px;
}
.heading h1 {
  color: #263f8f;
  font-size: 60px;
  font-weight: 900;
  line-height: 82px;
  letter-spacing: 2px;
  animation-name: h1-animate;
  animation-duration: 2s;
}
.heading h2 {
  color: #00263b;
  font-size: 45px;
  font-weight: bold;
  line-height: 40px;
  margin-bottom: 12px;
  letter-spacing: 2px;
  animation-name: h2-animate;
  animation-duration: 2s;
}

/* viruses */

.viruses {
  animation: rotation 8s infinite linear;
  position: absolute;
}

.virus-1 {
  width: 50px;
  top: 10vh;
  right: 300px;
  /* animation: inhale 8s infinite linear; */
}
.virus-2 {
  width: 90px;
  top: 80vh;
  right: 500px;
}

.virus-3 {
  width: 40px;
  top: 37vh;
  right: 100px;
}

@keyframes h1-animate {
  from {
    opacity: 0;
    margin-left: -50px;
  }
  to {
    opacity: 1;
    margin-left: 0px;
  }
}
@keyframes h2-animate {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@media only screen and (max-width: 500px) {
  .nav {
    margin: 10px 0px 0px 30px;
  }
  .title {
    font-size: 18px;
    font-weight: 500;
    color: #353535;
    letter-spacing: 1px;
  }

  .heading {
    margin-left: 35px;
    margin-top: 60px;
  }
  .heading h1 {
    color: #263f8f;
    font-size: 50px;
    font-weight: 900;
    line-height: 52px;
    letter-spacing: 1.5px;
  }
  .heading h2 {
    font-size: 40px;
    margin-bottom: 5px;
    line-height: 45px;
  }
  .virus-1 {
    width: 30px;
    top: 80vh;
    right: 150px;
    /* animation: inhale 8s infinite linear; */
  }
  .virus-2 {
    display: none;
  }
  .virus-3 {
    width: 45px;
    top: 60vh;
    right: 100px;
  }
}

@keyframes rotation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}
@keyframes inhale {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}
</style>