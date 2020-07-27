<template>
  <div id="NavBar">
    <div class="title">
      <img src="../assets/malolosLogo.png" alt />
      <h3>MALOLOS INFORMATION</h3>
    </div>

    <div class="side-menu">
      <a href="#">View Cases</a>
      <v-btn color="#00a1ab">Download App</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style scoped>
#NavBar {
  position: fixed;
  top: 0;
  width: 100vw;
  height: 70px;
  display: flex;
  justify-content: space-between;
  padding: 0px 70px 0px 70px;
}
.title {
  display: flex;
  align-items: center;
}
.title img {
  height: 50px;
  width: 50px;
  margin-right: 10px;
}
.title h3 {
  color: #f6eedf;
  font-weight: 450;
  letter-spacing: 1.5px;
}

.side-menu {
  display: flex;
  align-items: center;
}
.side-menu a {
  color: #00263b;
  text-decoration: none;
  font-size: 18px;
  margin-right: 30px;
}
.side-menu button {
  background: #00a1ab;
  color: #f6eedf;
  padding: 7px 13px 7px 13px;
  font-size: 18px;
  border-radius: 9px;
}
@media only screen and (max-width: 800px) {
  .side-menu {
    display: none;
  }
  .title img {
    height: 35px;
    width: 35px;
    margin-right: 10px;
  }
  .title h3 {
    color: #f6eedf;
    font-weight: 400;
    font-size: 18px;
    letter-spacing: 1px;
  }
  #NavBar {
    height: 60px;
  }
}

@media only screen and (max-width: 500px) {
  .title h3 {
    font-size: 16px;
    letter-spacing: 0.5px;
  }
  #NavBar {
    padding: 0px 30px 0px 30px;
  }
}
</style>