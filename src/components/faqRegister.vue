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

const registration = computed(() => {
  const array = [
    {
      e1: t('faq.reg.b1.e1'),
      e2: t('faq.reg.b1.e2'),
      e3: t('faq.reg.b1.e3'),
    },

    {
      e1: t('faq.reg.b2.e1'),
      e2: t('faq.reg.b2.e2'),
      u: {
        e1: t('faq.reg.b2.u.e1'),
        e2: t('faq.reg.b2.u.e2'),
        e3: t('faq.reg.b2.u.e3'),
      },
    },

    {
      e1: t('faq.reg.b3.e1'),
      e2: t('faq.reg.b3.e2'),
      u: {
        e1: t('faq.reg.b3.u.e1'),
        e2: t('faq.reg.b3.u.e2'),
        e3: t('faq.reg.b3.u.e3'),
        e4: t('faq.reg.b3.u.e4'),
        e5: t('faq.reg.b3.u.e5'),
        e6: t('faq.reg.b3.u.e6'),
        e7: t('faq.reg.b3.u.e7'),
        e8: t('faq.reg.b3.u.e8'),
        e9: t('faq.reg.b3.u.e9'),
        e10: t('faq.reg.b3.u.e10'),
        e11: t('faq.reg.b3.u.e11'),
        e12: t('faq.reg.b3.u.e12'),
      },
    },

    {
      e1: t('faq.reg.b4.e1'),
      ug: {
        e1: t('faq.reg.b4.u.e1'),
        e2: t('faq.reg.b4.u.e2'),
        e3: t('faq.reg.b4.u.e3'),
        e4: t('faq.reg.b4.u.e4'),
        e5: t('faq.reg.b4.u.e5'),
        e6: t('faq.reg.b4.u.e6'),
        e7: t('faq.reg.b4.u.e7'),
        e8: t('faq.reg.b4.u.e8'),
        e9: t('faq.reg.b4.u.e9'),
        e10: t('faq.reg.b4.u.e10'),
        e11: t('faq.reg.b4.u.e11'),
        e12: t('faq.reg.b4.u.e12'),
        e13: t('faq.reg.b4.u.e13'),
        e14: t('faq.reg.b4.u.e14'),
        e15: t('faq.reg.b4.u.e15'),
        e16: t('faq.reg.b4.u.e16'),
        e17: t('faq.reg.b4.u.e17'),
        e18: t('faq.reg.b4.u.e18'),
        e19: t('faq.reg.b4.u.e19'),
        e20: t('faq.reg.b4.u.e20'),
        e21: t('faq.reg.b4.u.e21'),
        e22: t('faq.reg.b4.u.e22'),
        e23: t('faq.reg.b4.u.e23'),
        e24: t('faq.reg.b4.u.e24'),
        e25: t('faq.reg.b4.u.e25'),
        e26: t('faq.reg.b4.u.e26'),
        e27: t('faq.reg.b4.u.e27'),
        e28: t('faq.reg.b4.u.e28'),
        e29: t('faq.reg.b4.u.e29'),
        e30: t('faq.reg.b4.u.e30'),
        e31: t('faq.reg.b4.u.e31'),
        e32: t('faq.reg.b4.u.e32'),
        e33: t('faq.reg.b4.u.e33'),
        e34: t('faq.reg.b4.u.e34'),
        e35: t('faq.reg.b4.u.e35'),
        e36: t('faq.reg.b4.u.e36'),
        e37: t('faq.reg.b4.u.e37'),
        e38: t('faq.reg.b4.u.e38'),
      },
    },

    {
      e1: t('faq.reg.b5.e1'),
      e2: t('faq.reg.b5.e2'),
    },
  ]
  return array
})
</script>

<template>
  <section>
    <h3 v-text="t('faq.reg.e1')" />

    <article v-for="(item, i) in registration" @click="setActive(i)">
      <span>
        <h4>{{ item.e1 }}</h4>

        <svg :class="{ cross: selectedItem == i }">
          <use xlink:href="../assets/sprite/icons.svg#plus" />
        </svg>
      </span>

      <span v-if="selectedItem == i" :class="{ border: selectedItem == i }">
        <p>{{ item.e2 }}</p>

        <p>
          {{ item.e3 }}
        </p>

        <ul v-if="item.u" v-for="ul in item.u">
          <li>{{ ul }}</li>
        </ul>

        <ul class="grid" v-if="item.ug">
          <li v-for="ul in item.ug">{{ ul }}</li>
        </ul>
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
