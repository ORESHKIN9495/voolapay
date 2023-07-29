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
        <h4 v-text="t('business.acc.b1.e1')" />

        <p v-text="t('business.acc.b1.e2')" />
      </span>

      <picture>
        <img src="@/assets/images/accaunt.png" alt="/" />
      </picture>
    </article>

    <article>
      <picture>
        <img class="phone" src="../assets/images/app.png" alt="app" />
      </picture>

      <span>
        <h4 v-text="t('business.acc.b2.e1')" />

        <p v-text="t('business.acc.b2.e2')" />
      </span>
    </article>

    <article>
      <span>
        <h4 v-text="t('business.acc.b3.e1')" />

        <p v-text="t('business.acc.b3.e2')" />
      </span>

      <picture>
        <img src="@/assets/images/countries.svg" alt="/" />
      </picture>
    </article>
  </section>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
section {
  article {
    &:first-child {
      picture {
        img {
          max-width: 500px;
        }
      }
    }

    &:nth-child(2) {
      @media only screen and (max-width: 720px) {
        & {
          picture {
            order: 1;
          }
        }
      }
    }
  }
}
</style>
