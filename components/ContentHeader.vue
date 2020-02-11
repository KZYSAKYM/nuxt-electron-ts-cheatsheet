<template>
  <section id="header" class="hero is-dark is-small">
    <div class="hero-body">
      <LogoDark />
      <p class="title">
        Nuxt Electron Typescript Cheet Sheet
      </p>
      <p class="subtitle">
        and, Bulma CSS Framework cheet sheet
      </p>
    </div>
  </section>
</template>

<script lang="ts">
import LogoDark from '~/components/LogoDark.vue';
import { Component, Vue } from 'nuxt-property-decorator';

@Component({
  components: {
    LogoDark,
  },
})

export default class extends Vue { }
</script>

<style>
</style>
