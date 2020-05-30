<template>
  <div @scroll="changeClass" id="App">
    <Nav :change="Scrolled" />
    <Header id="Home" />
    <Services id="Services" />
    <Team id="Portfolio" />
  </div>
</template>

<script>
import Nav from "./components/Nav";
import Header from "./components/Header";
import Services from "./components/Services";
import Team from "./components/Team";

export default {
  name: "App",
  components: {
    Nav,
    Header,
    Services,
    Team
  },
  data() {
    return {
      postion: window.scrollY,
      Scrolled: false
    };
  },
  methods: {
    changeClass() {
      /* this.postion = window.scrollY */
      this.postion = document.documentElement.scrollTop;
      if (this.postion >= 100) {
        this.Scrolled = !this.Scrolled;
      }
    }
  }
};
</script>

<style lang="scss">
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
}

.container {
  width: 85%;
  height: 100%;
  margin: 0 auto;
}
</style>
