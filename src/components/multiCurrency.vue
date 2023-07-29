<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="grid">
    <picture>
      <img src="../assets/images/multi-currency.png" alt="account" />
    </picture>

    <div>
      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#arrow-repeat" />
        </svg>

        <span>
          <h4 v-text="t('multi-currency.b1.e1')" />

          <p v-text="t('multi-currency.b1.e2')" />
        </span>
      </article>

      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#coin" />
        </svg>

        <span>
          <h4 v-text="t('multi-currency.b2.e1')" />

          <p v-text="t('multi-currency.b2.e2')" />
        </span>
      </article>

      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#lightning" />
        </svg>

        <span>
          <h4 v-text="t('multi-currency.b3.e1')" />

          <p v-text="t('multi-currency.b3.e2')" />
        </span>
      </article>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  picture {
    img {
      box-shadow: 30px 28px 30px -14px #0000004d;
      border-radius: 12px;
    }

    @media (max-width: 720px) {
      & {
        order: 1;
      }
    }
  }

  div {
    display: grid;
    gap: calc(var(--section-gap) * 2);

    article {
      align-items: center;
      display: grid;
      grid-template-columns: 50px 1fr;
      gap: var(--section-gap);
    }
  }
}
</style>
