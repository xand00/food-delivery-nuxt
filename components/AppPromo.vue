<template>
    <div class="app-promo">
      <div class="background"></div>
      <h5 class="name text--secondary">Food app</h5>
      <p class="title text">Why stay hungry when you can order form Bella Onojie</p>
      <h4 class="description text--secondary">Download the bella onoje's food app now on</h4>
      <app-download-buttons />
      <div class="image">
        <img src="~assets/img/app-promo/phones-food-for-you-and-everyone.png" alt="">
      </div>
    </div>
</template>

<style lang="scss" scoped>
    .app-promo {
        display: flex;
        align-items: center;
        flex-direction: column;
        width: 100%;
        padding: 3.125rem 0.75rem 0 0.75rem;
        position: relative;

        @media (min-width: 64em) {
            color: white;
        }
        
        .background {
            width: 100%;
            @media (min-width: 64em) {            
                background-image: url('~assets/img/app-promo/background.png');
                background-repeat: no-repeat;
                background-origin: border-box;
                background-size: contain;
                background-position: center;
                position: absolute;
                top: -10rem;
                overflow-y: hidden;
                z-index: -1;
                height: 38.625rem;
                width: 100%;
                max-width: 90rem;

            }
        }



        .name {
            font-weight: 700;
            line-height: 0.6em;
            margin-bottom: 1rem;

            @media (min-width: 64em) {
                color: white;
            }
        }

        .title {
            font-weight: 700;
            font-size: 2rem;
            margin-bottom: 1.625rem;

            @media (min-width: 64em) {
                color: white;
            }
        }

        .description {
            font-size: 1.5rem;
            font-weight: 500;
            line-height: 2rem;
            margin-bottom: 3.125rem;

            @media (min-width: 64em) {
                color: white;
            }
        }
    }
</style>