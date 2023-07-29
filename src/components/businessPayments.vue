<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import Backward from '../components/Backward.vue'

const { t } = useI18n()
</script>

<template>
  <section>
    <article>
      <span>
        <h4 v-text="t('business.pay.b1.e1')" />

        <p v-text="t('business.pay.b1.e2')" />
      </span>
    </article>

    <article>
      <picture>
        <img src="../assets/images/guard.svg" alt="guard" />
      </picture>

      <span>
        <h4 v-text="t('business.pay.b2.e1')" />

        <p v-text="t('business.pay.b2.e2')" />
      </span>
    </article>

    <article>
      <span>
        <h4 v-text="t('business.pay.b3.e1')" />

        <p v-text="t('business.pay.b3.e2')" />
      </span>

      <picture>
        <img src="../assets/images/card.png" alt="card" />
      </picture>
    </article>

    <article>
      <span>
        <figure>66</figure>

        <p v-text="t('business.pay.b4.e1')" />
      </span>

      <span>
        <figure>7</figure>

        <p v-text="t('business.pay.b4.e2')" />
      </span>

      <span>
        <figure>9.3</figure>

        <p v-text="t('business.pay.b4.e3')" />
      </span>
    </article>

    <article>
      <picture>
        <img src="../assets/images/phones.svg" alt="phones" />
      </picture>

      <span>
        <h4 v-text="t('business.pay.b5.e1')" />

        <p v-text="t('business.pay.b5.e2')" />
      </span>
    </article>
  </section>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
section {
  article {
    &:first-child {
      background: var(--scheme-color-v3);
      border-radius: var(--scheme-radius);
      box-shadow: var(--scheme-shadow);
      grid-template-columns: 1fr;
      padding: calc(var(--section-gap) * 4);
      text-align: center;
      p {
        text-align: center;
      }

      h4 {
        color: var(--color-theme);
      }

      @media only screen and (max-width: 720px) {
        & {
          padding: calc(var(--section-gap) * 2);
        }
      }
    }

    &:nth-child(3) {
      picture {
        justify-self: center;

        img {
          max-width: 450px;
        }

        @media only screen and (max-width: 720px) {
          & {
            order: -1;
          }
        }
      }
    }

    &:nth-child(4) {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: var(--section-gap);

      span {
        display: grid;
        justify-items: center;

        figure {
          font-size: 40px;
          width: 200px;
          height: 200px;
        }

        p {
          max-width: 300px;
          text-align: center;
        }
      }

      @media only screen and (max-width: 720px) {
        & {
          grid-template-columns: 1fr;
        }
      }
    }
  }
}
</style>
