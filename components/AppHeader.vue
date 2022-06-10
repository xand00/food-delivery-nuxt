<template>
    <header class="header">
        <div class="header-container">
            <div class="logo">
                <app-logo />
            </div>
            <nav class="menu">
                <div class="options">
                    <nuxt-link :class="`option ${ $nuxt.$route.$path === option.path ? 'active' : '' }`" v-for="option in this.optionList" :to="option.path" :key="option.name">
                        {{ option.name }}
                    </nuxt-link>
                </div>
                <button class="hamburger-button unstyled-button">
                    <app-burger-button />
                </button>
            </nav>
        </div>
    </header>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    data() {
        return {
            optionList: [
                {
                    name: 'Home',
                    path: '/',
                },
                {
                    name: 'Product',
                    path: '/product',
                },
                {
                    name: 'Faq',
                    path: '/faq',
                },
                {
                    name: 'Contact',
                    path: '/contact',
                },
            ]
        }
    }
})
</script>

<style lang="scss" scoped>
    .header {
        background-color: white;

        .header-container {
            @media (min-width: 64em) {
                min-height: 9.75rem;
            }

            margin: auto;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            min-height: 7rem;
            padding: 1rem 3.125rem;
            max-width: 90rem;
    
            .logo {
                @media (min-width: 64em) {
                    margin-left: 2.5rem;
                }
            }
    
            .menu {
                display: flex;
                align-items: center;
    
                .options {
                    display: none;
    
                    @media (min-width: 64em) {
                        display: flex;
                        column-gap: 7.125rem;
    
                        a {
                            text-decoration: none;
                            color: black;   
                            display: inline-block;
                            font-weight: 600;
                            font-size: 1rem;
                            line-height: 1.75rem;
                            letter-spacing: 0.0125rem;
                            
    
                            &:hover {
                                transform: scale(1.1);
                                transition: all 0.1s;
                                -webkit-backface-visibility: hidden; 
                                backface-visibility: hidden; 
                            }
                            
                            &.nuxt-link-exact-active {
                                color: $primary-color;
                            }
                        }
                    }
                }
    
                .hamburger-button {
                    @media (min-width: 64em) {
                        display: none;
                    }
                }
    
            }

        }
    }

    
</style>