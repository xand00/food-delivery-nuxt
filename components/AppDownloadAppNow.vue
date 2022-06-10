<template>
    <div class="download-the-app-now">
      <div class="background"></div>
      <p class="title">
        Download the app now.
      </p>
      <p class="description-mobile">
        Most calendars are designed for teams. 
      </p>
      <p class="description-desktop">
        Available on your favorite store. Start your premium experience now
      </p>
      <div class="buy-or-try-buttons">
        <a href="https://play.google.com/" class="first" target="_blank">
          <app-button
            :buttonFontSize="'1rem'"
            :buttonBorderRadius="'10px'"
          >
            Buy now
          </app-button>
        </a>
        <a href="https://play.google.com/" target="_blank">
          <app-button
            class="second"
            :buttonFontSize="'1rem'"
            :buttonBorderRadius="'10px'"
            colorScheme="transparent-secondary"
          >
            Try for free
          </app-button>
        </a>
      </div>
      <div class="download-buttons">
        <a href="https://play.google.com/" target="_blank">
            <app-button
              :buttonFontSize="'1rem'"
              :buttonBorderRadius="'10px'"
            >
              Playstore
            </app-button>
        </a> 
        <a href="https://www.apple.com/store" target="_blank">
            <app-button
              :buttonFontSize="'1rem'"
              :buttonBorderRadius="'10px'"
              colorScheme="transparent-secondary"
              class="color-dynamic-button">
              App store
            </app-button>
        </a>
      </div>
    </div>
</template>

<style scoped lang="scss">
    .download-the-app-now {
        background-color: $secondary-color;
        padding: 3.375rem 2.5rem;
        letter-spacing: 0.0125rem;
        width: 100%;

        display: flex;
        flex-direction: column;
        align-items: center;

        @media (min-width: 64em) {
          background-color: transparent;
          background-repeat: no-repeat;
          background-position: center;
          background-image: url('~assets/img/download-the-app-now/background.png');

          
        }

        .title {
            color: white;
            margin-bottom: 1.25rem;
            font-weight: 700;
            font-size: 2.5rem;
            line-height: 3.5rem;
        }

        .description-mobile {
            color: #BDBDBD;
            margin-bottom: 4rem;
            font-weight: 500;
            font-size: 1.5rem;
            line-height: 2.375rem;
            @media (min-width: 64em) {
              display: none;
            }
        }

        .description-desktop {
            color: white;
            margin-bottom: 4rem;
            font-weight: 500;
            font-size: 1.5rem;
            line-height: 2.375rem;
            display: none;
            @media (min-width: 64em) {
              display: block;
            }
        }

        .buy-or-try-buttons {
            display: flex;
            flex-direction: row;
            column-gap: 1rem;
            width: 100%;
            @media (min-width: 64em) {
              display: none;

              max-width: 20rem;
            }

            a {
              width: 100%;
            }

            .first {
              flex-shrink: 1.35;
            }
        }

        .download-buttons {
          display: flex;
          flex-direction: row;
          column-gap: 1rem;
          width: 100%;
          display: none;
          a {
            width: 100%;
          }
          @media (min-width: 64em) {
            display: flex;

            max-width: 20rem;
          }
        }
    }
</style>