<template>
    <div class="container">
        <nuxt-link to="/">
            <nuxt-img src="logo.png" loading="lazy" alt="Logo" />
        </nuxt-link>
    </div>
</template>

<style lang="scss" scoped>
    .container {
        width: 100%;
    }

    img {
        max-width: 6.5rem;

        @media (min-width: 64rem) {
            max-width: 100%;
        }
    }
</style>