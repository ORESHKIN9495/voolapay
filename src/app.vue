<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { watch, ref } from 'vue'

import { useI18n } from 'vue-i18n'

import { useRouter } from 'vue-router'

import headerNav from '@/components/headerNav.vue'
import footerNav from '@/components/footerNav.vue'

const { t, locale } = useI18n()

const router = useRouter()

const currentLocale = ref(locale.value)

watch(router.currentRoute, (route) => {
  currentLocale.value = route.params.locale as string
})

watch(currentLocale, (val) => {
  router.push({
    name: router.currentRoute.value.name!,
    params: { locale: val },
  })
})
</script>

<template>
  <headerNav />

  <router-view />

  <footerNav :t="t" :locale="locale" />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300&family=Noto+Sans:wght@300&display=swap');

@font-face {
  font-family: CoFoSans-Regular;
  src: url(./assets/font/CoFoSans-Regular.otf);
}

@font-face {
  font-family: CoFoSans-Mediun;
  src: url(./assets/font/CoFoSans-Medium.otf);
}

@font-face {
  font-family: CoFoSans-Bold;
  src: url(./assets/font/CoFoSans-Bold.otf);
}

@import url('https://cdn.jsdelivr.net/gh/lipis/flag-icons@6.9.2/css/flag-icons.min.css');

/* semantic color variables for this project */
:root {
  --scheme-color-v1: #21252a;

  --scheme-color-v2: #1d2024;

  --scheme-color-v3: #31353d;

  --scheme-color-v4: #2a2e32;

  --scheme-radius: 20px;

  --scheme-shadow: 0 30px 20px -20px rgba(0, 0, 0, 0.3019607843);

  --color-text: #ffffff;

  --color-theme: #4e94d7;

  --font: 15px;

  --font-family: 'CoFoSans-Regular', 'Noto Sans', 'Noto Sans SC', sans-serif;

  --section-gap: 20px;

  --section-width: 1420px;

  --scheme-color-text: #ffffff60;

  --scheme-size-l: clamp(50px, 6vw, 72px);

  --scheme-size-m: clamp(30px, 6vw, 42px);
}

/*
  resset
*/

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

a {
  color: inherit;
  text-decoration: none;
}

body {
  background-color: var(--scheme-color-v1);
  color: var(--color-text);
  font: 300 var(--font) / 1.64 var(--font-family);
  transition: color 0.3s, background-color 0.3s;
}

h1 {
  font: 300 var(--scheme-size-l) / 1.32 var(--font-family);

  span {
    color: var(--color-theme);
  }
}

h3 {
  font: 300 var(--scheme-size-m) / 1.32 var(--font-family);
}

h4 {
  font: 300 18px / 1.32 var(--font-family);
}

img {
  display: inherit;
  width: 100%;
}

p {
  color: var(--scheme-color-text);
  text-align: justify;
}

picture {
  display: inline-block;
}

::selection {
  background: #4e95d720;
}

svg {
  fill: var(--color-theme);
  height: 40px;
  width: 40px;
}

.phone {
  border: 5px solid var(--scheme-color-v2);
  border-radius: 35px;
  box-shadow: 30px 28px 30px -14px #0000004d;
  max-width: 220px !important;
}
</style>
