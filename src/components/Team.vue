<template>
  <section>
    <div class="container">
      <div class="wrapper">
        <img src="../assets/top-view-photo-of-people-near-wooden-table.jpg" :alt="alt" />
        <div class="content">
          <h2>{{ title }}</h2>
          <p>{{desc}}</p>
          <p>{{desc}}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Team",
  data() {
    return {
      title: "our team",
      desc:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde odio nemo eius voluptas dolores velit similique illo nobis dolor nostrum, reiciendis fuga iste inventore, in maxime. Rerum, sequi error ipsam assumenda quae et voluptate aliquid accusantium, soluta beatae quos, nostrum culpa possimus facere iure dolorem enim reiciendis porro maxime a",
      src: "../assets/top-view-photo-of-people-near-wooden-table.jpg",
      alt: "Team Work"
    };
  }
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  height: 70vh;
  background: #223546;
  color: #fff;
  padding: 50px 0;
}
img {
  width: 700px;
}
h2{
  font-size: 1.6rem;
  text-transform: uppercase;
  margin: 40px 0;
}
p{
  font-size: 1.3rem;
  margin-bottom: 20px;
}
.wrapper {
  width: 100%;
  margin: 50px auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(700px, 1fr));
}
</style>