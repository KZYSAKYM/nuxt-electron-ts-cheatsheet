<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        nuxt-electron-ts-template
      </h1>
      <h2 class="subtitle">
        Template of Nuxt-Electron-Typescript
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
        <a
          href="/"
          target="_self"
          class="button--red"
        >
          Normal
        </a>
      </div>
      <br><br><ContentHeader />
    </div>
  </div>
</template>

<script lang="ts">
import Logo from '~/components/Logo.vue';
import ContentHeader from '~/components/ContentHeader.vue';
import { Component, Vue } from 'nuxt-property-decorator';

@Component({
  components: {
    ContentHeader,
    Logo,
  },
})

export default class extends Vue { }
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
