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

const current = computed(() => {
  const array = [
    {
      e1: t('faq.curr.b1.e1'),
      e2: t('faq.curr.b1.e2'),
    },

    {
      e1: t('faq.curr.b2.e1'),
      e2: t('faq.curr.b2.e2'),
    },

    {
      e1: t('faq.curr.b3.e1'),
      e2: t('faq.curr.b3.e2'),
      u: {
        e1: t('faq.curr.b3.u.e1'),
        e2: t('faq.curr.b3.u.e2'),
        e3: t('faq.curr.b3.u.e3'),
        e4: t('faq.curr.b3.u.e4'),
        e5: t('faq.curr.b3.u.e5'),
      },
      e3: t('faq.curr.b3.e3'),
    },

    {
      e1: t('faq.curr.b4.e1'),
      e2: t('faq.curr.b4.e2'),
    },
  ]

  return array
})
</script>

<template>
  <section class="faq_current_acc">
    <h3 v-text="t('faq.curr.e1')" />

    <article v-for="(item, i) in current" :key="i" @click="setActive(i)">
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
  background: var(--scheme-color-v2);
}
</style>
