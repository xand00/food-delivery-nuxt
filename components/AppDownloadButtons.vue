<template>
    <div class="buttons">
        <a href="https://play.google.com/" target="_blank">
            <app-button>Playstore</app-button>
        </a> 
        <a href="https://www.apple.com/store" target="_blank">
            <app-button colorScheme="transparent-primary" class="color-dynamic-button">App store</app-button>
        </a>
    </div>
</template>

<style lang="scss" scoped>
    .buttons {
        a {
            width: 100%;
        }
        
        max-width: 14.75rem;
        display: flex;
        flex-direction: column;
        row-gap: 1rem;
        width: 100%;

        .color-dynamic-button {
            @media (min-width: 64em) {
                color: white;
                border-color: white;

            }
        }

        @media (min-width: 64em) {
            flex-direction: row;
            max-width: 32rem;
            column-gap: 2rem;
        }
    }
</style>