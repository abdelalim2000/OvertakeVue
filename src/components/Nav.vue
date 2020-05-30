<template>
  <header class="/*scrolled:Scrolled */ scrolled">
    <div class="container">
      <div class="logo">OverTake</div>
      <nav>
        <ul>
          <li v-for="(item, index) in links" :key="index" class="nav-item">
            <a :href="item.des" class="nav-link">{{ item.name }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Nav",
  props: ["Scrolled"],
  data() {
    return {
      links: [
        {
          des: "#Home",
          name: "Home"
        },
        {
          des: "#About",
          name: "About US"
        },
        {
          des: "#Services",
          name: "Services"
        },
        {
          des: "#Portfolio",
          name: "Portfolio"
        },
        {
          des: "#Pricing",
          name: "Pricing"
        },
        {
          des: "#Contact",
          name: "Contact"
        }
      ]
    };
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  height: 7vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #fff;
  color: #223546;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10;
}
.logo {
  font-size: 2rem;
  text-transform: uppercase;
  position: relative;
  height: 100%;
  padding: 10px 20px;

  &::after {
    content: "Consulting";
    font-size: 0.9rem;
    position: absolute;
    bottom: 0%;
    right: 11%;
  }
}

ul {
  display: flex;
  justify-content: space-between;
  align-items: center;

  li {
    list-style: none;

    a {
      text-decoration: none;
      color: #223546;
      padding: 15px 30px;
      text-transform: uppercase;
      transition: all 0.3s ease-in;

      &:hover {
        background: #223546;
        color: #fff;
      }
    }
  }
}
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.scrolled {
  background: #223546;
  color: #fff;

  .logo::after {
    color: #fff;
  }
  .nav-link {
    color: #fff;

    &:hover {
      background: #fff;
      color: #223546;
    }
  }
}
</style>