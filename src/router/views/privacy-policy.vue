<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
import { useI18n } from 'vue-i18n'

// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import Backward from '../components/Backward.vue'

const { t, locale } = useI18n()
</script>

<template>
  <main>
    <section>
      <h1 v-text="t('privacy.e1')" />
    </section>

    <section>
      <article>
        <p v-text="t('privacy.b1.e1')" />
        <p v-text="t('privacy.b1.e2')" />
        <p v-text="t('privacy.b1.e3')" />

        <h4 v-text="t('privacy.b2.e1')" />

        <p v-text="t('privacy.b2.e2')" />
        <p v-text="t('privacy.b2.e3')" />
        <p v-text="t('privacy.b2.e4')" />
        <p v-text="t('privacy.b2.e5')" />
        <p v-text="t('privacy.b2.e6')" />

        <h4 v-text="t('privacy.b3.e1')" />

        <p v-text="t('privacy.b3.e2')" />

        <h4 v-text="t('privacy.b4.e1')" />

        <p v-text="t('privacy.b4.e2')" />
        <p v-text="t('privacy.b4.e3')" />

        <h4 v-text="t('privacy.b5.e1')" />

        <p v-text="t('privacy.b5.e2')" />
        <p v-text="t('privacy.b5.e3')" />
        <p v-text="t('privacy.b5.e4')" />

        <ul>
          <li v-text="t('privacy.b5.u1.e1')" />
          <li v-text="t('privacy.b5.u1.e2')" />
          <li v-text="t('privacy.b5.u1.e3')" />
          <li v-text="t('privacy.b5.u1.e4')" />
          <li v-text="t('privacy.b5.u1.e5')" />
          <li v-text="t('privacy.b5.u1.e6')" />
        </ul>

        <p v-text="t('privacy.b5.e5')" />

        <ul>
          <li v-text="t('privacy.b5.u2.e1')" />
          <li v-text="t('privacy.b5.u2.e2')" />
        </ul>

        <p v-text="t('privacy.b5.e6')" />

        <ul>
          <li v-text="t('privacy.b5.u3.e1')" />
          <li v-text="t('privacy.b5.u3.e2')" />
          <li v-text="t('privacy.b5.u3.e3')" />
          <li v-text="t('privacy.b5.u3.e4')" />
          <li v-text="t('privacy.b5.u3.e5')" />
        </ul>

        <p v-text="t('privacy.b5.e7')" />

        <ul>
          <li v-text="t('privacy.b5.u4.e1')" />
          <li v-text="t('privacy.b5.u4.e2')" />
          <li v-text="t('privacy.b5.u4.e3')" />
          <li v-text="t('privacy.b5.u4.e4')" />
          <li v-text="t('privacy.b5.u4.e5')" />
        </ul>

        <p v-text="t('privacy.b5.e8')" />

        <ul>
          <li v-text="t('privacy.b5.u5.e1')" />
          <li v-text="t('privacy.b5.u5.e2')" />
        </ul>

        <p v-text="t('privacy.b5.e9')" />

        <ul>
          <li v-text="t('privacy.b5.u6.e1')" />
          <li v-text="t('privacy.b5.u6.e2')" />
          <li v-text="t('privacy.b5.u6.e3')" />
          <li v-text="t('privacy.b5.u6.e4')" />
          <li v-text="t('privacy.b5.u6.e5')" />
          <li v-text="t('privacy.b5.u6.e6')" />
          <li v-text="t('privacy.b5.u6.e7')" />
          <li v-text="t('privacy.b5.u6.e8')" />
          <li v-text="t('privacy.b5.u6.e9')" />
          <li v-text="t('privacy.b5.u6.e10')" />
          <li v-text="t('privacy.b5.u6.e11')" />
        </ul>

        <p v-text="t('privacy.b5.e10')" />

        <ul>
          <li v-text="t('privacy.b5.u7.e1')" />
          <li v-text="t('privacy.b5.u7.e2')" />
          <li v-text="t('privacy.b5.u7.e3')" />
          <li v-text="t('privacy.b5.u7.e4')" />
          <li v-text="t('privacy.b5.u7.e5')" />
        </ul>

        <p v-text="t('privacy.b5.e11')" />
        <p v-text="t('privacy.b5.e12')" />
        <p v-text="t('privacy.b5.e13')" />

        <h4 v-text="t('privacy.b6.e1')" />

        <p v-text="t('privacy.b6.e2')" />

        <ul>
          <li v-text="t('privacy.b6.u.e1')" />
          <li v-text="t('privacy.b6.u.e2')" />
          <li v-text="t('privacy.b6.u.e3')" />
          <li v-text="t('privacy.b6.u.e4')" />
          <li v-text="t('privacy.b6.u.e5')" />
          <li v-text="t('privacy.b6.u.e6')" />
        </ul>

        <h4 v-text="t('privacy.b7.e1')" />

        <p>{{ t('privacy.b7.e2') }} <a href="mailto:dpo@xwardpay.io">dpo@xwardpay.io</a>.</p>

        <h4 v-text="t('privacy.b8.e1')" />

        <p v-text="t('privacy.b8.e2')" />

        <h4 v-text="t('privacy.b9.e1')" />

        <p v-text="t('privacy.b9.e2')" />

        <ul>
          <li v-text="t('privacy.b9.u.e1')" />
          <li v-text="t('privacy.b9.u.e2')" />
          <li v-text="t('privacy.b9.u.e3')" />
          <li v-text="t('privacy.b9.u.e4')" />
          <li v-text="t('privacy.b9.u.e5')" />
          <li v-text="t('privacy.b9.u.e6')" />
          <li v-text="t('privacy.b9.u.e7')" />
          <li v-text="t('privacy.b9.u.e8')" />
          <li v-text="t('privacy.b9.u.e9')" />
        </ul>

        <p v-text="t('privacy.b9.e3')" />

        <h4 v-text="t('privacy.b10.e1')" />

        <p v-text="t('privacy.b10.e2')" />
        <p v-text="t('privacy.b10.e3')" />
        <p v-text="t('privacy.b10.e4')" />
        <p v-text="t('privacy.b10.e5')" />
        <p v-text="t('privacy.b10.e6')" />

        <ul>
          <li v-text="t('privacy.b10.u.e1')" />
          <li v-text="t('privacy.b10.u.e2')" />
        </ul>

        <h4 v-text="t('privacy.b11.e1')" />

        <p v-text="t('privacy.b11.e2')" />

        <h4 v-text="t('privacy.b12.e1')" />

        <p v-text="t('privacy.b12.e2')" />
        <p v-text="t('privacy.b12.e3')" />
        <p v-text="t('privacy.b12.e4')" />
        <p v-text="t('privacy.b12.e5')" />

        <h4 v-text="t('privacy.b13.e1')" />

        <p v-text="t('privacy.b13.e2')" />

        <ol>
          <li v-text="t('privacy.b13.o.e1')" />
          <li v-text="t('privacy.b13.o.e2')" />
          <li v-text="t('privacy.b13.o.e3')" />
          <li v-text="t('privacy.b13.o.e4')" />
          <li v-text="t('privacy.b13.o.e5')" />
          <li v-text="t('privacy.b13.o.e6')" />
          <li v-text="t('privacy.b13.o.e7')" />
          <li v-text="t('privacy.b13.o.e8')" />
          <li v-text="t('privacy.b13.o.e9')" />
        </ol>

        <p>{{ t('privacy.b13.e2') }} <a href="mailto:dpo@xwardpay.io">dpo@hawex.com</a></p>

        <h4 v-text="t('privacy.b14.e1')" />

        <p v-text="t('privacy.b14.e2')" />
        <p v-text="t('privacy.b14.e3')" />
        <p v-text="t('privacy.b14.e4')" />
        <p v-text="t('privacy.b14.e5')" />

        <h4 v-text="t('privacy.b15.e1')" />

        <p v-text="t('privacy.b15.e2')" />
        <p v-text="t('privacy.b15.e3')" />
        <p v-text="t('privacy.b15.e4')" />

        <h4 v-text="t('privacy.b16.e1')" />

        <ul>
          <li v-text="t('privacy.b16.u1.e1')" />
        </ul>

        <p v-text="t('privacy.b16.e2')" />

        <ul>
          <li v-text="t('privacy.b16.u2.e1')" />
        </ul>

        <p v-text="t('privacy.b16.e3')" />

        <ul>
          <li v-text="t('privacy.b16.u3.e1')" />
        </ul>

        <p v-text="t('privacy.b16.e4')" />

        <ul>
          <li v-text="t('privacy.b16.u4.e1')" />
        </ul>

        <p v-text="t('privacy.b16.e5')" />

        <h4 v-text="t('privacy.b17.e1')" />

        <p v-text="t('privacy.b17.e2')" />

        <p v-text="t('privacy.b17.e3')" />
      </article>
    </section>
  </main>
</template>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang="scss">
main {
  padding: var(--section-gap);

  section {
    max-width: var(--section-width);
    margin: auto;

    a {
      color: var(--color-theme);
    }

    article {
      h4 {
        font-family: CoFoSans-Bold;
        text-transform: uppercase;
      }

      p {
        margin: var(--section-gap) 0;
      }

      ul {
        line-height: 2;
        list-style-position: inside;
        margin: var(--section-gap) 0;
      }

      ol {
        line-height: 2;
        list-style-position: inside;
        margin: var(--section-gap) 0;
      }
    }
  }
}
</style>
