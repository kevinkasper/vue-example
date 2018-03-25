<template>
    <article class="c-card">
        <header class="c-card__header">
            <div class="c-card__image" style="background-image: url('https://placehold.it/350x200')"></div>
        </header>
        <div class="c-card__body">
            <h2 class="c-card__title">Card</h2>
            <p class="c-card__subtitle">initial component</p>
            <p class="c-card__intro">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
        </div>
        <footer class="c-card__footer">
            Footer
        </footer>
    </article>
</template>

<script lang="ts">
import { Component } from 'vue-property-decorator';
import Vue from 'vue';

@Component({
    name: 'card',
})
export default class Card extends Vue {

}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/bootstrap';

    .c-card {
        box-shadow: 0 6px 10px -5px rgba(0, 0, 0, .2);
        cursor: pointer;
        display: flex;
        flex: 0 1 350px;
        flex-direction: column;
        margin: 20px;
        text-align: left;
        transition: $global-transition;

        &:hover {
            box-shadow: 0 20px 20px -15px rgba(0, 0, 0, .3);
            transform: translateY(-5px);
        }

        &__body {
            padding: 20px;
        }
        
        &__footer {
            border-top: 1px solid $color-very-light-grey;
            padding: 20px;
        }

        &__image {
            background-position: center center;
            background-size: cover;
            background-repeat: no-repeat;
            height: 200px;
        }

        &__intro {
            margin-bottom: 0;
        }

        &__title {
            font-size: 15px;
            font-weight: 700;
            line-height: 1.2;
            margin: 0;
            padding: 0;
            text-transform: uppercase;
        }

        &__subtitle {
            font-size: 13px;
            margin-top: 5px;
            padding: 0;
        }
    }

    .c-card--center {
        text-align: center;
    }

    .c-card--right {
        text-align: right;
    }

    .c-card--wide {
        flex: 0 1 740px;
        flex-direction: row;
        flex-wrap: wrap;

        .c-card {
            &__body {
                flex: 1;
                padding-top: 30px;
            }

            &__footer {
                flex: 1 1 100%;
                text-align: center;
            }

            &__header {
                flex: 1;
            }
        }
    }
</style>