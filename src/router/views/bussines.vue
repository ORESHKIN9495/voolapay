<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import Backward from '../components/Backward.vue'

import businessAccaunt from '@/components/businessAccaunt.vue'
import businessPayments from '@/components/businessPayments.vue'
import businessDevelop from '@/components/businessDevelop.vue'

const { t } = useI18n()
</script>

<template>
  <main>
    <h1 v-html="t('business.e1')" />

    <businessAccaunt />
    <businessPayments />
    <businessDevelop />
  </main>
</template>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style lang="scss" scoped>
main:deep() {
  margin: auto;
  max-width: var(--section-width);
  padding: var(--section-gap);

  h1 {
    margin: calc(var(--section-gap) * 4) 0 0;
    max-width: 600px;

    span {
      color: var(--color-theme);
    }
  }

  h3 {
    span {
      color: var(--color-theme);
    }
  }

  p {
    margin: var(--section-gap) 0 0;
  }

  svg {
    width: 100%;
    height: 100%;
  }

  h4 {
    text-transform: uppercase;
  }

  picture {
    img {
      max-width: 600px;
      margin: auto;
    }
  }

  section {
    margin: calc(var(--section-gap) * 6) 0 0;

    article {
      align-items: center;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: calc(var(--section-gap) * 2);
      margin: calc(var(--section-gap) * 4) 0 0;

      figure {
        align-items: center;
        background: var(--scheme-color-v3);
        box-shadow: var(--scheme-shadow);
        border-radius: 50%;
        color: var(--color-theme);
        display: flex;
        justify-content: center;
        max-width: 250px;
        margin: auto;
        padding: calc(var(--section-gap) * 2);
        width: 100%;
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
