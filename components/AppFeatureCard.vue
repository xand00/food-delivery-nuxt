<template>
    <div :class="`feature-card ${isReversed ? 'reversed' : ''}`">
        <div class="container">
            <p class="name">{{ name }}</p>
            <p class="title">{{ title }}</p>
            <p class="description">{{ description }}</p>
        </div>
        <img :src="require(`~/assets/img/${imageSrc}`)">
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    props: {
        name: String,
        title: String,
        description: String,
        imageSrc: String,
        isReversed: Boolean
    }
})
</script>

<style lang="scss" scoped>
    .feature-card {
        display: flex;
        flex-direction: column;

        
        
        @media (min-width: 64em) {
            flex-direction: row-reverse;

            &:nth-child(even) {
                flex-direction: row;

                .container {
                    @media (min-width: 64em) {
                        padding: 0 0 0 15rem;
                    }
                }
            }

        }

        .container {
            padding: 0 2.25rem;

            @media (min-width: 64em) {
                padding: 0 10rem 0 0;

                display: flex;
                flex-direction: column;
                align-items: flex-start;
                justify-content: center;
                text-align: left;
            }

            .name {
                color: $primary-color;
                font-weight: 700;
                font-size: 1.5rem;
                line-height: 2.25rem;
                letter-spacing: 0.00625rem;
                margin-bottom: 2.5rem;
            }

            .title {
                color: $secondary-color;
                font-weight: 700;
                font-size: 2.5rem;
                line-height: 3.5rem;
                letter-spacing: 0.0125rem;
                margin-bottom: 3.125rem;
            }

            .description {
                color: $tertiary-color;
                font-weight: 500;
                font-size: 1.5rem;
                line-height: 2.375rem;
                letter-spacing: 0.0125;
            }
        }

        img {
            width: 100%;

            @media (min-width: 64em) {
                min-width: 36rem;
            }
        }
    }
</style>