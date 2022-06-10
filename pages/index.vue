<template>
  <div class="page-container">
    <app-promo class="index-promo" />
    <app-section-separator>How the app works</app-section-separator>
    <app-app-features class="app-features" />
    <app-download-app-now />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>

<style lang="scss">
  .page-container {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    row-gap: 1em;
  }

  .index-promo {
    margin-bottom: 8rem;
  }

  img {
    width: 100%;
  }

  .text {
    color: $secondary-color;
  }

  .text--secondary {
    color: $tertiary-color;
  }
</style>
