<template>
    <div class="container">
        <app-navigation></app-navigation>
        <app-page-one></app-page-one>
        <app-between></app-between>
        <app-page-two></app-page-two>
    </div>
</template>

<script>
import Navigation from "./components/Navigation.vue";
import PageOne from "./components/PageOne.vue";
import Between from "./components/Between.vue";
import PageTwo from "./components/PageTwo.vue";

    export default {
        components: {
            'app-navigation': Navigation,
            'app-page-one': PageOne,
            'app-between': Between,
            'app-page-two': PageTwo,
        }
        
    }
</script>

<style>
@import 'resources/css/style.css';
</style>
