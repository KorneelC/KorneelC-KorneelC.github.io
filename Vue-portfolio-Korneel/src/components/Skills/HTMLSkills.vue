<template>
 <div class="row">
    <app-project :titleId="html1" :title="titleHtmlProject" :link="linkHtml" :descriptionWork="descriptionHtmlProject"></app-project>
 </div>
</template>

<script>
    import project from './project.vue'
    export default {
         data() {
            return {
                html1: 'html',
                titleHtmlProject:'HTML Basics',
                linkHtml: 'html/index.html',
                descriptionHtmlProject: 'This a project where I learned the basics of HTML5. I had to rebuild the excercise webpage'
            }
        },  
        components: {
            'app-project':project
        }   
        
    }
</script>

<style scoped>

</style>