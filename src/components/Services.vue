<template>
  <section id="#Services">
    <div class="container">
      <h2>{{title}}</h2>
      <p>{{desc}}</p>
      <div class="wrapper">
        <div v-for="(card, index) in cards" :key="index" class="card">
          <i :class="card.img"></i>
          <h3 class="title">{{ card.header }}</h3>
          <p class="desc">{{ card.desc }}</p>
          <button class="btn">Learn More</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Services",
  data() {
    return {
      title: "Services",
      desc:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde odio nemo eius voluptas dolores velit similique illo nobis dolor nostrum, reiciendis fuga iste inventore, in maxime. Rerum, sequi error ipsam assumenda quae et voluptate aliquid accusantium, soluta beatae quos, nostrum culpa possimus facere iure dolorem enim reiciendis porro maxime",
      cards: [
        {
          img: "fas fa-cog",
          header: "IT Strategy",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde odio nemo eius voluptas dolores velit similique"
        },
        {
          img: "far fa-clipboard",
          header: "Products",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde odio nemo eius voluptas dolores velit similique"
        },
        {
          img: "fas fa-user-alt",
          header: "Development",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde odio nemo eius voluptas dolores velit similique"
        },
        {
          img: "fas fa-home",
          header: "Quality",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde odio nemo eius voluptas dolores velit similique"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
#Services {
  width: 100%;
  background: #fff;
  text-align: center;
  margin: 70px 0 30px;
}

h2 {
  text-transform: uppercase;
  color: #223546;
  font-size: 2.2rem;
}
.wrapper {
  width: 80%;
  margin: 100px auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
}

.card {
  padding: 50px 10px;
  border-radius: 15px;
  background: #223546;
  margin-bottom: 10px;
  width: 270px;

  h3 {
    color: #fff;
    font-size: 1.5rem;
    margin: 30px 0;
  }
  p {
    color: #fff;
    font-size: 1.1rem;
    margin: 30px 0;
  }
}
.btn {
  background: #fff;
  border-radius: 5px;
  color: #223546;
  outline: none;
  border: none;
  padding: 15px 30px;
  margin-top: 30px;
  cursor: pointer;
  font-size: 0.9rem;
}
i {
  font-size: 3.6rem;
  color: #fff;
}
</style>