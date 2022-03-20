<template>
  <div class="wheel_wrap">
    <h1>Easier vue-wheel</h1>
    <Wheel
      ref="wheel"
      :gift="gift"
      :data="data"
      @done="done"
      :imgParams="logo"
      @click="spinTheWheel"
    />
  </div>
</template>

<script>
import { Wheel } from "vue3-fortune-wheel";
import "vue3-fortune-wheel/dist/library.css";

export default {
  name: "App",
  components: {
    Wheel,
  },
  data() {
    return {
      gift: 1,
      logo: {
        width: 100,
        height: 120,
        src: "/public/bnb.png",
      },
      data: [
        {
          id: 1,
          value: "Gift 1",
          bgColor: "#7d7db3",
          color: "#ffffff",
        },
        {
          id: 2,
          value: "Gift 2",
          bgColor: "#ffffff",
          color: "#000000",
        },
        {
          id: 3,
          value: "Gift 3",
          bgColor: "#c92729",
          color: "#ffffff",
        },
        {
          id: 4,
          value: "Gift 4",
          bgColor: "#7d7db3",
          color: "#ffffff",
        },
        {
          id: 5,
          value: "Gift 5",
          bgColor: "#ffffff",
          color: "#000000",
        },
        {
          id: 6,
          value: "Gift 6",
          bgColor: "#c92729",
          color: "#ffffff",
        },
      ],
    };
  },
  methods: {
    done(params) {
      console.log(params);
    },
    spinTheWheel() {
      this.$refs.wheel.spin();
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.wheel_wrap {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
