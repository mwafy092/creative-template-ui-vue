<template>
  <section class="portfolio">
    <div class="portfolio__title">OUR PORTFOLIO</div>
    <div class="portfolio__text">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit aliquam at libero
      justo maecenas nibh tortor, mollis ac arcu vitae.
    </div>
    <div class="portfolio__tabs">
      <button
        @click="(e) => selectData('ALL', e)"
        class="portfolio__tabs--active"
      >
        ALL
      </button>
      <button @click="(e) => selectData('ILLUSTRATION', e)">
        ILLUSTRATION
      </button>
      <button @click="(e) => selectData('PHOTOGRAPHY', e)">PHOTOGRAPHY</button>
      <button @click="(e) => selectData('DESIGN', e)">DESIGN</button>
      <button @click="(e) => selectData('WALLPAPER', e)">WALLPAPER</button>
    </div>
    <div class="portfolio__tabs__container">
      <div
        class="portfolio__tabs__chunk"
        v-for="data in filteredStore"
        :key="data.id"
      >
        <div class="portfolio__chunks__active">
          <div class="portfolio__chunk__name__active">{{ data?.name }}</div>
          <div class="portfolio__chunk__category__active">
            {{ data?.category }}
          </div>
        </div>
        <div class="portfolio__chunk__img">
          <img :src="'/images/' + data?.img" />
        </div>
        <div class="portfolio__chunk__name">{{ data?.name }}</div>
        <div class="portfolio__chunk__category">{{ data?.category }}</div>
      </div>
    </div>
  </section>
</template>

<script>
import { getData } from "../data/api";

export default {
  data() {
    return {
      store: [],
      filteredStore: [],
      selectedSection: "all",
    };
  },
  methods: {
    selectData(category, e) {
      let parent = document.querySelector(".portfolio__tabs");
      for (let item of parent.children) {
        if (item === e?.target) {
          item.classList.add("portfolio__tabs--active");
        } else {
          item.classList.remove("portfolio__tabs--active");
        }
      }
      if (category.toLowerCase() !== "all") {
        this.filteredStore = this?.store.portfolio.filter(
          (p) => p.category.toLowerCase() === category.toLowerCase()
        );
      } else {
        this.filteredStore = this.store.portfolio;
      }
    },
  },
  mounted() {
    this.store = getData();
    this.filteredStore = this.store.portfolio;
  },
};
</script>
<style lang="scss">
@import "../assets/styles/portfolio.scss";
</style>
