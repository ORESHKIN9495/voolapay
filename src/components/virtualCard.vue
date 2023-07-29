<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="grid">
    <picture>
      <img class="phone" src="../assets/images/virtual-card.png" alt="virtual card" />
    </picture>

    <article>
      <h3 v-text="t('virtual-card.e1')" />

      <p v-text="t('virtual-card.e2')" />
    </article>
  </section>
</template>

<style scoped lang="scss">
section {
  h3 {
    font-family: CoFoSans-Bold;
    margin: calc(var(--section-gap) * 2) 0;
    text-transform: uppercase;
  }

  picture {
    @media (max-width: 720px) {
      & {
        order: 1;
      }
    }
  }
}
</style>
