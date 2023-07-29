<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs

import { computed, ref } from 'vue'
import { useI18n } from 'vue-i18n'

// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import Backward from '../components/Backward.vue'

const { t } = useI18n()

const selectedItem = ref()

const setActive = (i: number) => {
  if (selectedItem.value == null) {
    selectedItem.value = i
  } else {
    selectedItem.value = null
  }
}

const mastercard = computed(() => {
  const array = [
    {
      e1: t('faq.master.b1.e1'),
      e2: t('faq.master.b1.e2'),
    },

    {
      e1: t('faq.master.b2.e1'),
      e2: t('faq.master.b2.e2'),
    },

    {
      e1: t('faq.master.b3.e1'),
      e2: t('faq.master.b3.e2'),
      u: {
        e1: t('faq.master.b3.u.e1'),
        e2: t('faq.master.b3.u.e2'),
      },
      e3: t('faq.master.b3.e3'),
    },
  ]

  return array
})
</script>

<template>
  <section class="faq_mastercard">
    <h3 v-text="t('faq.master.e1')" />

    <article v-for="(item, i) in mastercard" :key="i" @click="setActive(i)">
      <span>
        <h4>{{ item.e1 }}</h4>

        <svg :class="{ cross: selectedItem == i }">
          <use xlink:href="../assets/sprite/icons.svg#plus" />
        </svg>
      </span>

      <span v-if="selectedItem == i">
        <p>{{ item.e2 }}</p>

        <ul v-if="item.u" v-for="ul in item.u">
          <li>{{ ul }}</li>
        </ul>

        <p>
          {{ item.e3 }}
        </p>
      </span>
    </article>
  </section>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
section {
  background: var(--scheme-color-v4);
}
</style>
