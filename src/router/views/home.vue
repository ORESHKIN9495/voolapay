<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs

import { useI18n } from 'vue-i18n'

// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import howItWorks from '@/components/howItWorks.vue'
import virtualCard from '@/components/virtualCard.vue'
import security from '@/components/security.vue'
import physicalCard from '@/components/physicalCard.vue'
import multyCurrency from '@/components/multiCurrency.vue'

const { t } = useI18n()
</script>

<template>
  <main>
    <section class="hero">
      <h1 v-html="t('home.e1')" />

      <p v-html="t('home.e2')" />

      <picture>
        <img src="@/assets/images/card-blue-logo.png" alt="card" />
      </picture>
    </section>

    <howItWorks />

    <virtualCard />

    <physicalCard />

    <multyCurrency />

    <security />
  </main>
</template>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang="scss">
main {
  section {
    margin: calc(var(--section-gap) * 4) auto 0;
    max-width: var(--section-width);
    position: relative;
    padding: var(--section-gap);

    picture {
      inset: 15% 0 auto auto;
      position: absolute;
      z-index: -1;

      img {
        border-radius: var(--scheme-radius);
        box-shadow: var(--scheme-shadow);
        max-width: 600px;
      }
    }

    h1 {
      max-width: 600px;
    }

    p {
      margin: var(--section-gap) 0;
      max-width: 532px;
    }

    @media (max-width: 720px) {
      & {
        picture {
          inset: 0;
          position: relative;
          z-index: 0;
        }
      }
    }

    &.grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: calc(var(--section-gap) * 2);
      max-width: var(--section-width);
      padding: var(--section-gap);
      place-items: center;

      @media (max-width: 720px) {
        & {
          grid-template-columns: 1fr;

          picture {
            img {
              margin: auto;
            }
          }
        }
      }
    }
  }
}
</style>
