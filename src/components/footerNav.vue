<script setup lang="ts">
defineProps<{ t: Function; locale: string }>()
</script>

<template>
  <footer>
    <nav>
      <router-link :to="{ name: 'privacy-policy', params: { locale } }" v-text="t('footer.e1')" />
      <a href="https://portal.vooladmcc.com/legal/terms" target="_blank" v-text="t('footer.e2')" />
      <a href="https://portal.vooladmcc.com/legal/termsofuse" target="_blank" v-text="t('footer.e3')" />

      <span>© 2023 VOOLA PAY</span>
    </nav>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  padding: var(--section-gap);

  nav {
    display: flex;
    gap: var(--section-gap);
    place-items: center baseline;
    margin: auto;
    max-width: var(--section-width);

    a {
      border: 2px solid;
      border-color: #0000;

      &:hover {
        border-color: #0000 #0000 var(--color-theme);
      }
    }

    span {
      color: #ffffff60;
      margin: 0 0 0 auto;
    }
  }

  @media (max-width: 720px) {
    nav {
      display: grid;

      span {
        margin: 0;
      }
    }
  }
}
</style>
