<template>
    <div id="app">
        <div class="card-container">
            <card></card>
            <card class="c-card--center"></card>
            <card class="c-card--right"></card>
            <card class="c-card--wide"></card>
        </div>
    </div>
</template>

<script lang="ts">
    import Card from './components/card.vue';
    import { Component } from 'vue-property-decorator';
    import Vue from 'vue';

    @Component({
        components: {
            Card,
        },
        name: 'app',
    })
    export default class App extends Vue {

    }
</script>

<style lang="scss">
    @import './assets/scss/bootstrap.scss';

    #app {
        height: 100vh;
    }

    .card-container {
        align-items: center;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        height: 100%;
        justify-content: center;

        > .c-card--wide {
            flex: 1 1 100%;
        }
    }
</style>