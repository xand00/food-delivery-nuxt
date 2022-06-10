<template>
    <div>
        <app-feature-card
            v-for="(appFeature, index) in this.appFeatures"
            v-bind="appFeature"
            :isReversed="index % 2 === 1"
            :key="appFeature.id"
        />
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'
    export default Vue.extend({
        data() {
            return {
                appFeatures: [
                    {
                    id: 1,
                    name: "Create an account",
                    title: "Create/login to an existing account to get started",
                    description: "An account is created with your email and a desired password",
                    imageSrc: "index-feature-cards-1.png",
                    },
                    {
                    id: 2,
                    name: "Explore while shopping",
                    title: "Shop for your favorites meal as e dey hot.",
                    description: "Shop for your favorite meals or drinks and enjoy while doing it.",
                    imageSrc: "index-feature-cards-2.png",
                    },
                    {
                    id: 3,
                    name: "Checkout",
                    title: "When you done check out and get it delivered.",
                    description: "When you done check out and get it delivered with ease.",
                    imageSrc: "index-feature-cards-3.png",
                    },
                ]
            }
        }
    })
</script>