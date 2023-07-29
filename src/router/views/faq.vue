<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs

import { useI18n } from 'vue-i18n'

// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import Backward from '../components/Backward.vue'

import faqRegister from '@/components/faqRegister.vue'
import faqCurrencyAcc from '@/components/faqCurrentAcc.vue'
import faqMastercard from '@/components/faqMastercard.vue'

const { t } = useI18n()
</script>

<template>
  <main>
    <h1 v-text="t('faq.e1')" />

    <faqRegister />

    <faqCurrencyAcc />

    <faqMastercard />
  </main>
</template>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang="scss">
main {
  max-width: var(--section-width);
  margin: auto;
  padding: var(--section-gap);

  h1 {
    margin: calc(var(--section-gap) * 4) 0 0;
  }

  section:deep() {
    border-radius: var(--scheme-radius);
    box-shadow: var(--scheme-shadow);
    margin: calc(var(--section-gap) * 2) 0;
    padding: var(--section-gap) calc(var(--section-gap) * 2);

    h3 {
      margin: var(--section-gap) 0;
    }

    article {
      padding: var(--section-gap) 0 0;

      span {
        border: none;
        display: inherit;
        gap: var(--section-gap);
        transition: transform 0.3s ease-in-out;

        &:first-child {
          align-items: center;
          border-bottom: 1px solid var(--scheme-color-v3);
          display: flex;
          justify-content: space-between;
          padding: 10px 0;
        }
      }

      &:last-child {
        span {
          &.border {
            border-bottom: 1px solid var(--scheme-color-v3);
          }

          &:last-child {
            border: none;
          }
        }
      }

      svg {
        fill: currentColor;
        min-width: 30px;
        transition: 0.3s ease-in-out;
        width: 30px;

        &.cross {
          fill: var(--color-theme);
          transform: rotate(45deg);
        }
      }

      h4 {
        color: #ccc;
      }

      p {
        margin: var(--section-gap) 0;
      }

      ul {
        line-height: 2;
        list-style-position: inside;
        padding: 0 var(--section-gap);

        &.grid {
          display: grid;
          grid-template: auto / repeat(3, 1fr);

          @media (max-width: 720px) {
            & {
              grid-template: auto / 1fr;
            }
          }
        }
      }
    }
  }
}
</style>
