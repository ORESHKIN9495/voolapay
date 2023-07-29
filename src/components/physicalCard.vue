<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section class="grid">
    <article>
      <h3 v-text="t('physical-card.e1')" />

      <p v-text="t('physical-card.e2')" />
    </article>

    <picture>
      <img class="phone" src="../assets/images/physical-card.png" alt="physical card" />
    </picture>
  </section>
</template>

<style scoped lang="scss">
section {
  h3 {
    font-family: CoFoSans-Bold;
    margin: calc(var(--section-gap) * 2) 0;
    text-transform: uppercase;
  }
}
</style>
