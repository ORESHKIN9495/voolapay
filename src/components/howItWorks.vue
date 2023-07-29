<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <section>
    <h3 v-text="t('how-it-works.e1')" />

    <div>
      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#speed" />
        </svg>

        <span>
          <h4 v-text="t('how-it-works.b1.e1')" />

          <p v-text="t('how-it-works.b1.e2')" />
        </span>
      </article>

      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#wallet" />
        </svg>

        <span>
          <h4 v-text="t('how-it-works.b2.e1')" />

          <p v-text="t('how-it-works.b2.e2')" />
        </span>
      </article>

      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#card" />
        </svg>

        <span>
          <h4 v-text="t('how-it-works.b3.e1')" />

          <p v-text="t('how-it-works.b3.e2')" />
        </span>
      </article>

      <article>
        <svg>
          <use xlink:href="../assets/sprite/icons.svg#globe" />
        </svg>

        <span>
          <h4 v-text="t('how-it-works.b4.e1')" />

          <p v-text="t('how-it-works.b4.e2')" />
        </span>
      </article>
    </div>
  </section>
</template>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang="scss">
section {
  background: var(--scheme-color-v3);
  display: grid;
  max-width: 100% !important;

  h3 {
    font-family: CoFoSans-Bold;
    margin: calc(var(--section-gap) * 2) auto;
    text-transform: uppercase;
  }

  div {
    display: grid;
    gap: var(--section-gap);
    grid-template-columns: repeat(2, 1fr);
    max-width: var(--section-width);
    margin: auto;
    place-items: baseline;

    article {
      align-items: center;
      display: grid;
      grid-template-columns: 50px 1fr;
      gap: var(--section-gap);
      padding: var(--section-gap) 0;

      svg {
        align-self: flex-start;
      }

      h4 {
        text-transform: uppercase;
      }

      p {
        margin: var(--section-gap) 0 0;
      }
    }
  }

  @media (max-width: 720px) {
    & {
      div {
        grid-template-columns: 1fr;
      }
    }
  }
}
</style>
