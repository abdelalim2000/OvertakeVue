<template>
  <main id="#Home">
    <div class="container">
      <h1>{{title}}</h1>
      <p>{{desc}}</p>
    </div>
  </main>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      title: "Strategy and design",
      desc:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, nemo."
    };
  }
};
</script>

<style lang="scss" scoped>
main {
  height: 100vh;
  width: 100%;
  background: linear-gradient(90deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("../assets/hot-air-balloons.jpg") no-repeat;
  background-size: cover;
  background-position: center cernter;
  background-attachment: fixed;
  position: relative;
}
h1 {
  position: absolute;
  bottom: 30%;
  color: #fff;
  text-transform: uppercase;
  font-size: 3.5rem;
  letter-spacing: 2px;
}
p {
  position: absolute;
  bottom: 25%;
  color: #fff;
  font-size: 1.2rem;
}
</style>