<template>
  <div class="layout">
    <app-header />
    <Nuxt />
    <app-footer />
  </div>
</template>

<style lang="scss">
    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
        font-family: 'Monsterrat', sans-serif;
    }

    html {
      overflow-y: scroll;
    }

    .layout {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      min-height: 100vh;
    }

    @font-face {
      font-family: 'Monsterrat';
      font-style: normal;
      font-weight: 400;
      font-display: swap;
      src: url('~/assets/fonts/Montserrat-Regular.ttf') format('truetype');
    }

    .unstyled {
        &-button {
            background: none;
            color: inherit;
            border: none;
            padding: 0;
            font: inherit;
            cursor: pointer;
            outline: inherit;
        }
    }
</style>