<script>
import fullp from "../assets/fullp.jpeg";
import fullp1 from "../assets/fullp1.jpeg";
import fullp2 from "../assets/fullp2.jpeg";
import fullp3 from "../assets/fullp3.jpeg";
import fullp4 from "../assets/fullp4.jpeg";
import fullp5 from "../assets/fullp5.jpeg";

export default {
  data() {
    return {
      fullp: fullp,
      fullp1: fullp1,
      fullp2: fullp2,
      fullp3: fullp3,
      fullp4: fullp4,
      fullp5: fullp5,
      change: 1,
    };
  },
  methods: {
    switchimg() {
      if (this.change == 1) {
        this.change = 2;
      } else if (this.change == 2) {
        this.change = 3;
      } else if (this.change == 3) {
        this.change = 4;
      } else if (this.change == 4) {
        this.change = 5;
      } else if (this.change == 5) {
        this.change = 6;
      } else {
        this.change = 1;
      }
    },
  },
};
</script>

<template>
  <div>
    <div v-if="change == 1">
      <img :src="fullp" alt="Panic1" />
    </div>
    <div v-else-if="change == 2">
      <img :src="fullp1" alt="Panic2" />
    </div>
    <div v-else-if="change == 3">
      <img :src="fullp2" alt="Panic3" />
    </div>
    <div v-else-if="change == 4">
      <img :src="fullp3" alt="Panic4" />
    </div>
    <div v-else-if="change == 5">
      <img :src="fullp4" alt="Panic5" />
    </div>
    <div v-else-if="change == 6">
      <img :src="fullp5" alt="Panic6" />
    </div>
    <div v-else>
      <img :src="fullp" alt="Panic1" />
    </div>
    <button @click="switchimg">Switch</button>
  </div>
</template>

<style>
img {
  height: 500px;
  width: 50%;
  border-style: ridge;
  border-width: 15px;
  border-color: blue red green yellow;
  border-radius: 25px;
  margin-top: 40px;
  margin-bottom: 20px;
  padding-top: 10px;
  padding-bottom: 10px;
  outline-style: groove;
  outline-color: cornflowerblue;
  outline-width: medium;
  outline-offset: 5px;
}

body {
  background-image: url("../assets/fullp6.jpeg");
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: 80% 50%;
  background-color: #cafafe;
}

button {
  border: 2px solid violet;
  background-color: rgb(255, 99, 71);
  color: darkblue;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  font-style: oblique;
  font-size: 30px;

  border-radius: 15px;
}
</style>
