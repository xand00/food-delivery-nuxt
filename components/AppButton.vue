<template>
    <button
        @click="$emit('click', $event)"
        :style="buttonStyle"
        :class="`unstyled-button button ${colorScheme ? 'button--' + colorScheme : '' }`">
        <slot />
    </button>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    props: {
        colorScheme: String,
        buttonFontSize: {
            type: String,
        },
        buttonBorderRadius: {
            type: String,
        }
    },
    data() {
        return {
            buttonStyle: {
                fontSize: this.buttonFontSize ?? '1.5rem',
                borderRadius: this.buttonBorderRadius ?? '30px',
            }
        }
    }
})
</script>

<style lang="scss" scoped>
    .button {
        background-color: $primary-color;
        color: white;
        padding: 1rem 0;
        width: 100%;
        font-weight: 700;
        line-height: 2.25rem;
        letter-spacing: 0.00625rem;
        max-height: 4rem;
    }

    .button--transparent-primary {
        background-color: transparent;
        color: $primary-color;
        border: 1px $primary-color solid;
    }

    .button--transparent-secondary {
        background-color: transparent;
        color: white;
        border: 1px white solid;
    }
</style>