<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section>
    <article>
      <h3 v-text="t('security.e1')" />

      <p v-text="t('security.e2') + ':'" />

      <ul>
        <li v-text="t('security.b1.e1')" />

        <li v-text="t('security.b1.e2')" />

        <li v-text="t('security.b1.e3')" />
      </ul>

      <p v-text="t('security.e3')" />

      <p v-text="t('security.e4')" />

      <a href="https://apps.apple.com/app/voola-pay/id6445897299" target="_blank">
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#apple" />
        </svg>
      </a>

      <a href="https://play.google.com/store/apps/details?id=com.vooladmcc.portal" target="_blank">
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#google" />
        </svg>
      </a>
    </article>
  </section>
</template>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang="scss">
section {
  background: var(--scheme-color-v3);
  padding: var(--section-gap);
  max-width: 100% !important;

  article {
    max-width: var(--section-width);
    margin: auto;

    p {
      margin: var(--section-gap) 0;
    }

    a {
      display: inline-block;
      margin: var(--section-gap) 0;

      &:last-child {
        margin-left: var(--section-gap);
      }

      svg {
        fill: #fff;

        &:hover {
          fill: var(--color-theme);
        }
      }
    }

    ul {
      line-height: 2;
      list-style-position: inside;
      padding: 0 var(--section-gap);
    }
  }
}
</style>
