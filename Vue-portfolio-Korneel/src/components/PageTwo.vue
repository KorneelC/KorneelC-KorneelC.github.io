<template>
    <div>
        <div class="parallax2" id="work-nav"></div>
        <div class="content1" data-aos="fade-down" data-aos-duration="700">
            <h2 class="title">{{myProjects}}</h2>
            <div class="btn-wrap">
                <button class="skill-btn" @click="Skills($event, 'app-HTML', 'HTML Projects')">HTML</button>
                <button class="skill-btn" @click="Skills($event,'app-CSS', 'CSS Projects')">CSS</button>
                <button class="skill-btn" @click="Skills($event,'app-SCSS', 'SCSS Projects' )">SCSS</button>
                <button class="skill-btn" @click="Skills($event,'app-JS', 'JavaScript Projects')">JAVASCRIPT</button>
                <button class="skill-btn" @click="Skills($event,'app-VUE', 'Vue.js Projects')">Vue.js</button>
            </div>
            <transition name="fade" mode="out-in">
                <component :is="selectedComponent"></component>
            </transition>
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
                myProjects: 'My Projects',                
            }
        },
        methods: {
            Skills: function (event,skill, project) {
                  let tablinks = document.getElementsByClassName("skill-btn");
                  for (let i = 0; i < tablinks.length; i++) {
                  tablinks[i].className = tablinks[i].className.replace(" color-btn", "");
                }
                event.currentTarget.className += " color-btn";
                this.selectedComponent = skill
                this.myProjects = project

            }

        },
         components: {
            'app-HTML':HTMLSkills,
            'app-CSS':CSSSkills,
            'app-SCSS':SCSSSkills,
            'app-JS':JavascriptSkills,
            'app-VUE':VueSkills,
            
        }
    }

</script>

<style scoped>
.skill-btn {
    border-radius: 12px;
}
.color-btn {
    background-color: aqua;
    color: white;
}
.color-btn:hover {
    color: white;
}
.fade-enter {
    opacity: 0;
}
.fade-enter-active {
    transition: opacity 2s;
}
</style>