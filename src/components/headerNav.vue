<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { watch, ref } from 'vue'

import { SUPPORT_LOCALES } from '../i18n'

import { useI18n } from 'vue-i18n'

import { useRouter } from 'vue-router'

const { t, locale } = useI18n()

const router = useRouter()

const visible = ref(false)

const changeLang = ref(false)

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
  <header>
    <nav>
      <router-link :to="{ name: 'home', params: { locale } }" @click="visible = false">
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#logo" />
        </svg>

        <small>+ PAY</small>
      </router-link>

      <svg @click="visible = !visible">
        <use xlink:href="../assets/sprite/icons.svg#dot" />
      </svg>

      <span :class="{ visible: visible }">
        <ul>
          <li>
            <router-link :to="{ name: 'bussines', params: { locale } }" @click="visible = false" v-text="t('header.e1')" />
          </li>

          <li>
            <router-link :to="{ name: 'faq', params: { locale } }" @click="visible = false" v-text="t('header.e2')" />
          </li>

          <li>
            <a href="https://portal.vooladmcc.com/auth" target="_blank" v-text="t('header.e3')" />
          </li>

          <li>
            <a href="https://portal.vooladmcc.com/auth/register/user" target="_blank" v-text="t('header.e4')" />
          </li>
        </ul>

        <ul>
          <li v-if="!changeLang && !visible" @click="changeLang = !changeLang" :class="`fi fi-${locale}`" />

          <li v-if="changeLang || visible" v-for="el of SUPPORT_LOCALES" :key="el" @click=";(currentLocale = el), (changeLang = false)" :class="`fi fi-${el}`" />
        </ul>
      </span>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
header {
  background-color: rgba(29, 32, 36, 0.9);
  box-shadow: var(--scheme-shadow);
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  inset: 0 auto auto;
  position: sticky;
  padding: var(--section-gap);
  z-index: 9;

  nav {
    display: flex;
    margin: auto;
    max-width: var(--section-width);

    svg {
      cursor: pointer;
      display: none;
      fill: currentColor;
      width: 80px;

      &:hover {
        fill: var(--color-theme);
      }

      @media only screen and (max-width: 820px) {
        display: inherit;
      }
    }

    a {
      svg {
        display: inherit;
      }

      &:first-child {
        display: flex;
        margin: 0 auto 0 0;

        small {
          color: #ccc;
        }
      }
    }

    span {
      display: flex;
      gap: var(--section-gap);

      &.visible {
        background: var(--scheme-color-v4);
        display: grid;
        place-items: center;
        position: absolute;
        padding: var(--section-gap);
        top: 80px;
        left: 0;
        right: 0;

        ul {
          display: flex !important;
        }
      }
    }

    ul {
      align-items: center;
      cursor: pointer;
      display: flex;
      gap: var(--section-gap);
      list-style: none;

      &:first-child:not(:last-child) {
        li {
          a:hover {
            border-bottom: 1.5px solid var(--color-theme);
          }

          &:nth-child(4) {
            border-radius: calc(var(--scheme-radius) - 10px);
            background: var(--scheme-color-v3);
            padding: 5px 20px;

            a {
              border: none;
            }

            &:hover {
              background: var(--color-theme);
            }
          }
        }
      }

      &:last-child {
        li {
          &.fi {
            background-size: 50px;
            border-radius: 50px;
            height: 30px;
            line-height: 1;
            width: 30px;
          }
        }
      }

      @media only screen and (max-width: 820px) {
        display: none;

        &:last-child {
          order: -1;
        }
      }
    }
  }
}
</style>
