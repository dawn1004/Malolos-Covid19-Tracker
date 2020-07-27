<template>
  <div class="standing">
    <div class="case">
      <p>Total Confirmed Cases:</p>
      <h1>45</h1>
    </div>
    <div class="bottom">
      <div class="deaths">
        <p>Deaths:</p>
        <h1>7</h1>
      </div>
      <div class="recovered">
        <p>Recovered</p>
        <h1>29</h1>
      </div>
    </div>

    <div class="container-date">
      <p>
        COVID-19 CORONAVIRUS PANDEMIC CASES IN MALOLOS
        <span>as of June 30, 2020</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Standing",
  created() {
    window.addEventListener("scroll", () => {
      let standing = document.querySelector(".standing");
      let standing_position = standing.getBoundingClientRect().top;
      console.log(standing_position);
      let screen_Position = window.innerHeight / 1.5;

      if (standing_position < screen_Position) {
        standing.classList.add("standing-appear");
      }
    });
  },
};
</script>

<style scoped>
.standing {
  background: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 830px;
  margin-left: 50vw;
  transform: translate(-50%, 50px);
  border-radius: 10px;
  margin-top: 100px;
  padding: 30px;

  opacity: 0;
  transition: 0.5s all ease-in-out;
}
.standing-appear {
  opacity: 1;
  transform: translate(-50%, 0px);
  width: 900px;
}
.bottom {
  display: flex;
  justify-content: space-around;
  width: 100%;
}
.standing p {
  font-size: 45px;
  font-weight: 900;
  color: #5a5555;
}
.standing h1 {
  text-align: center;
  font-size: 75px;
  font-weight: 900;
}
.case h1 {
  color: #aaaaaa;
}

.deaths h1 {
  color: #ff5d6c;
}
.recovered h1 {
  color: #8aca2b;
}
.container-date {
  margin-top: 20px;
}
.container-date p {
  font-size: 16px;
  font-weight: normal;
  font-style: italic;
}
.container-date span {
  color: rgb(95, 15, 15);
  text-transform: uppercase;
  font-style: italic;
}
</style>