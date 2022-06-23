<template>
  <section class="navbar">
    <div class="navbar__burger" @click="navSlide">
      <div class="navbar__burger__line1"></div>
      <div class="navbar__burger__line2"></div>
      <div class="navbar__burger__line3"></div>
    </div>
    <div class="navbar__logo">
      <a href="#">Safari</a>
    </div>
    <ul class="navbar__links">
      <li>
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#">About</a>
      </li>
      <li>
        <a href="#" @click="dropDownMenu">Portfolio</a>
        <div class="navbar__dropdown">
          <p>Illustration</p>
          <p>Photography</p>
          <p>Design</p>
          <p>Wallpaper</p>
        </div>
      </li>
      <li>
        <a href="#">Blog</a>
      </li>
      <li>
        <a href="#">Features</a>
      </li>
      <li>
        <a href="#">Pages</a>
      </li>
      <li>
        <a href="#">contact</a>
      </li>
    </ul>

    <div class="navbar__search">
      <img
        src="/icons/search-icon.svg"
        alt="search images"
        @click="setSearch"
      />
      <form class="navbar__search__popup">
        <input type="text" placeholder="search here" />
        <img src="/icons/search-icon.svg" alt="search images" />
      </form>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    dropDownMenu() {
      console.log("clicked");
      document
        .querySelector(".navbar__dropdown")
        .classList.toggle("navbar__dropdown--active");
    },
    setSearch() {
      document
        .querySelector(".navbar__search__popup")
        .classList.toggle("navbar__popup--active");
    },
    navSlide() {
      const burger = document.querySelector(".navbar__burger");
      const nav = document.querySelector(".navbar__links");
      const navLinks = document.querySelectorAll(".navbar__links li");
      nav.classList.toggle("navbar__links--active");
      navLinks.forEach((link, index) => {
        if (link.style.animation) {
          link.style.animation = "";
        } else {
          link.style.animation = `navbarLinkFade 0.9s ease forwards ${
            index / 7 + 0.5
          }s`;
        }
      });
      burger.classList.toggle("navbar__burger__toggle");
    },
  },
};
</script>

<style lang="scss">
@import "../assets/styles/navbar.scss";
</style>
