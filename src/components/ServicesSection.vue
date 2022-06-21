<template>
  <section class="services">
    <div class="services__container">
      <div
        class="services__chunk"
        v-for="(service, index) in store?.services"
        :key="index"
      >
        <div class="services__chunk__icon">
          <img :src="'/icons/' + service?.icon" alt="pencil icon" />
        </div>
        <p class="services__chunk__title">{{ service.title }}</p>
        <ul class="services__chunk__features">
          <li v-for="(feature, index) in service?.features" :key="index">
            {{ feature }}
          </li>
        </ul>
      </div>
    </div>
    <div class="services__buttons">
      <button>BUY THEME</button>
      <div class="services__buttons__sep">OR</div>
      <button>VIEW DEMO</button>
    </div>
  </section>
</template>

<script>
import { getData } from "../data/api";

export default {
  data() {
    return {
      store: [],
    };
  },

  mounted() {
    this.store = getData();
  },
};
</script>

<style lang="scss">
@import "../assets/styles/services.scss";
</style>
