<template>
    <footer class="footer">
        <div class="container">
            <div class="logo">
                <app-logo />
            </div>
            <div class="social-media-list">
                <a target="_blank" :href="socialMediaItem.url" v-for="socialMediaItem in this.socialMediaList" :key="socialMediaItem.url">
                    <img :src="socialMediaItem.iconPath">
                </a>
            </div>
            <div class="phrase">
                Just type what's on your mind and we'll 
            </div>
        </div>
    </footer>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    data() {
        return {
            socialMediaList: [
                {
                    iconPath: '/social-media-icon-list-linkedin.svg',
                    url: 'https://linkedin.com',
                },
                {
                    iconPath: '/social-media-icon-list-linkedin.svg',
                    url: 'https://linkedin.com',
                },
                {
                    iconPath: '/social-media-icon-list-linkedin.svg',
                    url: 'https://linkedin.com',
                },
            ]
        }
    }
})
</script>

<style lang="scss" scoped>
    .footer {
        width: 100%;
        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            row-gap: 0.75rem;
            padding: 4rem 5rem 2.5rem 5rem;
    
            @media (min-width: 64em) {
                flex-direction: row;
                align-items: center;
                justify-content: space-between;
                max-width: 90rem;
                width: 100%;
                margin: auto;
                padding: 4rem 5rem 2.5rem 5rem;
            }
    
            .logo {
                display: none;
    
                @media (min-width: 64em) {
                    display: block;
                    flex: 1;
                }
            }
    
            .social-media-list {
                display: flex;
                flex-direction: row;
                justify-content: center;
                column-gap: 2rem;
            }
    
            .phrase {
                font-weight: 700;
                font-size: 0.75rem;
                line-height: 1rem;
                letter-spacing: 0.00625rem;
                flex: 1;
                text-align: center;

                @media (min-width: 64em) {
                    text-align: right;
                }
            }
        }
    }
    
</style>