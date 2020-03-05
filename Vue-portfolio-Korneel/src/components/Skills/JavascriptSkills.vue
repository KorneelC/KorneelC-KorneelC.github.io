<template>
 <div class="row">
    <app-project :titleId="js1" :title="titleSnakeProject" :link="linkSnakeProject" :descriptionWork="descriptionSnakeProject"></app-project>
    <app-project :titleId="js2" :title="titleRpgProject" :link="linkRpgProject" :descriptionWork="descriptionRpgProject"></app-project>
    <app-project :titleId="js3" :title="titleFormProject" :link="linkFormProject" :descriptionWork="descriptionFormProject"></app-project>
</div>
</template>

<script>
    import project from './project.vue'
    export default {
         data() {
             return {
                js1: 'snake',
                js2: 'rpg',
                js3 : 'form',
                titleSnakeProject:'Snake',
                titleRpgProject: 'RPG',
                titleFormProject: 'Form',
                linkSnakeProject: 'snake/index.html',
                linkRpgProject: 'rpg/index.html',
                linkFormProject: 'form/index.html',
                descriptionSnakeProject: 'My personal snake project. I made this working snake version using JavaScript. Play this old but nostalgic game now!',
                descriptionRpgProject: 'In this exercise I made a turn based rpg game using JavaScript. It requires 2 players in order to play it.',
                descriptionFormProject: 'A working form with the use of Javascript and HTML5'
            }
        },
        components: {
            'app-project': project
        }    
        
    }
</script>

<style scoped>

</style>