<template>
  <h1>{{ title }}</h1>
  <!-- <ButtonApp @click="increment" type="button">Click me</ButtonApp>
  <DirectivesTest></DirectivesTest> -->
  <StarRatin :rating="4" />
</template>

<script>
// import ButtonApp from "./components/Button.vue";
// import DirectivesTest from "./components/DirectivesTest.vue";
import StarRatin from "./components/StarRatin.vue";
export default {
  name: "App",
  components: {
    // ButtonApp,
    // DirectivesTest,
    StarRatin,
  },
  data() {
    return {
      amountOfClicks: 0,
    };
  },
  computed: {
    title() {
      return `Amount of clicks ${this.amountOfClicks}`;
    },
  },
  methods: {
    increment() {
      this.amountOfClicks += 1;
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
</style>
