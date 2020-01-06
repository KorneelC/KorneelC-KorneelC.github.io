<template>
    <div>
        <div class="parallax2" id="work-nav"></div>
        <div class="content1">
            <h2 class="title">{{MyProjects}}</h2>
            <div class="btn-wrap">
                <button class="skill-btn" @click="selectedComponent = 'app-HTML', MyProjects = 'HTML Projects'">HTML</button>
                <button class="skill-btn" @click="selectedComponent = 'app-CSS', MyProjects = 'CSS Projects'">CSS</button>
                <button class="skill-btn" @click="selectedComponent = 'app-SCSS', MyProjects = 'SCSS Projects'">SCSS</button>
                <button class="skill-btn" @click="selectedComponent = 'app-JS', MyProjects = 'Javascript Projects'">JAVASCRIPT</button>
                <button class="skill-btn" @click="selectedComponent = 'app-VUE', MyProjects = 'Vue Projects'">Vue.js</button>
            </div>
            <component :is="selectedComponent"></component>
        </div>
    </div>
</template>

<script>
    import HTMLSkills from './Skills/HTMLSkills.vue';
    import CSSSkills from './Skills/CSSSkills.vue';
    import SCSSSkills from './Skills/ScssSkills.vue';
    import JavascriptSkills from './Skills/JavascriptSkills.vue';
    import VueSkills from './Skills/VueSkills.vue';
    export default {
        data () {
            return {
                selectedComponent: '',
                MyProjects: 'My Projects',
            }
        },
         components: {
            'app-HTML': HTMLSkills,
            'app-CSS': CSSSkills,
            'app-SCSS':SCSSSkills,
            'app-JS':JavascriptSkills,
            'app-VUE':VueSkills,
            
        }
    }
</script>

<style scoped>


</style>