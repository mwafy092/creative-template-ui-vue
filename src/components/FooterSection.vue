<template>
  <section class="footer">
    <div class="footer__contact">
      <p class="footer__contact__title">STAY IN TOUCH</p>
      <p class="footer__contact__text">
        Nunc a urna sed neque fermentum pharetra. Aliquam suscipit purus nisi
        convallis nulla.
      </p>
      <div class="footer__contact__social">
        <div
          class="footer__contact__social__icon"
          v-for="(data, index) in store.footer?.social"
          :key="index"
        >
          <img :src="'/icons/' + data" :alt="data" />
        </div>
      </div>
      <div class="footer__contact__text">
        <div class="footer__contact__text__chunk">
          <p>LOCATION</p>
          <p>4456 Bee Street</p>
          <p>Hoxeyville, MI 49641</p>
        </div>
        <div class="footer__contact__text__chunk">
          <p>CONTACTS</p>
          <p>231-862-1037</p>
          <p>youremail@support.com</p>
        </div>
      </div>
    </div>
    <div class="footer__flicker">
      <p>FLICKER FEED</p>
      <div class="footer__flicker__feeds">
        <img
          v-for="(data, index) in store?.footer?.flicker"
          :key="index"
          :src="'/images/' + data + '.png'"
        />
      </div>
    </div>
    <div class="footer__tweets">
      <p class="footer__tweets__title">TWEETS</p>
      <div class="footer__tweets__container">
        <div class="footer__tweet">
          <div class="footer__tweet__content">
            <img src="/icons/twitter-blue.png" alt="twitter" />
            <p class="footer__tweet__text">
              Nunc a urna sed neque ferment pharetra. purus nisi convallis
              nulla.
            </p>
          </div>
          <div class="footer__tweet__info">
            <span class="tweet__date">2 days ago</span>
            <span class="tweet__user">@esmeth</span>
          </div>
        </div>
        <div class="footer__tweet">
          <div class="footer__tweet__content">
            <img src="/icons/twitter-blue.png" alt="twitter" />
            <p class="footer__tweet__text">
              Nunc a urna sed neque ferment pharetra. purus nisi convallis
              nulla.
            </p>
          </div>
          <div class="footer__tweet__info">
            <span class="tweet__date">2 days ago</span>
            <span class="tweet__user">@esmeth</span>
          </div>
        </div>
        <div class="footer__tweet">
          <div class="footer__tweet__content">
            <img src="/icons/twitter-blue.png" alt="twitter" />
            <p class="footer__tweet__text">
              Nunc a urna sed neque ferment pharetra. purus nisi convallis
              nulla.
            </p>
          </div>
          <div class="footer__tweet__info">
            <span class="tweet__date">2 days ago</span>
            <span class="tweet__user">@esmeth</span>
          </div>
        </div>
      </div>
    </div>
    <div class="footer__categories">
      <p class="footer__categories__title">CATEGORIES</p>
      <p class="footer__categories__item">
        <img src="/icons/footer-arrow.png" alt="footer arrow" />
        Theme Features
      </p>
      <p class="footer__categories__item">
        <img src="/icons/footer-arrow.png" alt="footer arrow" />
        Web Development
      </p>
      <p class="footer__categories__item">
        <img src="/icons/footer-arrow.png" alt="footer arrow" />
        Social Networks
      </p>
      <p class="footer__categories__item">
        <img src="/icons/footer-arrow.png" alt="footer arrow" />
        iOS Applications
      </p>
      <p class="footer__categories__item">
        <img src="/icons/footer-arrow.png" alt="footer arrow" />
        eCommerce
      </p>
      <p class="footer__categories__item">
        <img src="/icons/footer-arrow.png" alt="footer arrow" />
        Post Formats
      </p>
    </div>
  </section>
  <section class="footer__bottom">
    <p>2013 © Unify. ALL Rights Reserved.</p>
    <p>Designed by PsdBooster</p>
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
@import "../assets/styles/footer.scss";
</style>
