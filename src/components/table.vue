<template>
  <v-container fluid class="container">
    <v-card width="900" class="main-table">
      <v-card-title>
        CASES BY BARANGAY
        <v-spacer></v-spacer>
        <v-text-field
          v-model="search"
          append-icon="mdi-magnify"
          label="Search"
          single-line
          hide-details
        ></v-text-field>
      </v-card-title>
      <v-data-table :headers="headers" :items="brgy_record" :search="search"></v-data-table>
    </v-card>
  </v-container>
</template>

<script>
import axios from "axios";

export default {
  name: "Table",
  data() {
    return {
      search: "",
      headers: [
        {
          text: "Barangay",
          align: "start",
          sortable: true,
          value: "brgy",
        },
        { text: "Confirm Cases", value: "confirmed_cases" },
        { text: "Recovered", value: "recovered" },
        { text: "Home Quarantine", value: "home_quarantine" },
        { text: "Hospitalized", value: "hospitalized" },
        { text: "Gov. Facility", value: "gov_facility" },
      ],
      brgy_record: [],
    };
  },
  created() {
    axios
      .get("https://maloloscovid.herokuapp.com/malolostracer")
      .then((response) => {
        console.log(response.data);
        this.brgy_record = response.data;
      });

    window.addEventListener("scroll", () => {
      let container = document.querySelector(".container");
      let container_position = container.getBoundingClientRect().top;
      console.log(container_position);
      let screen_Position = window.innerHeight / 1.3;

      if (container_position < screen_Position) {
        container.classList.add("container-appear");
      }
    });
  },
};
</script>

<style scoped>
.container {
  padding: 50px 0px 50px 0px;
  transform: translateY(50px);
  opacity: 0;
  transition: 0.5s all ease-in-out;
}
.container-appear {
  opacity: 1;
  transform: translateY(0px);
}
.main-table {
  margin-left: 50%;
  transform: translateX(-50%);
  padding: 20px;
  border-radius: 20px;
}

@media only screen and (max-width: 500px) {
  .table {
    display: none;
  }
}
</style>