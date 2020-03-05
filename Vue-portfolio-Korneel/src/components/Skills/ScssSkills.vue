<template>
 <div class="row">
    <app-project :titleId="scss1" :descriptionWork="descriptionClientProject" :title="titleMobile" :link="linkMobile"></app-project>
    <app-project :titleId="scss2" :descriptionWork="descriptionClientProject" :title="titleMultipage" :link="linkMultipage"></app-project>
    <app-project :titleId="scss3" :descriptionWork="descriptionClientProject" :title="titleClientProject" :link="linkClientProject"></app-project>
</div>
</template>

<script>
import project from './project.vue'
    export default {
         data () {
            return {
                scss1: 'admin',
                scss2: 'lol',
                scss3 : 'project',
                titleClientProject:'Client Project',
                titleMultipage: 'Multipage',
                titleMobile: 'Mobile version',
                linkMobile: 'admin/index.html',
                linkMultipage: 'multipage/korneel.html',
                linkClientProject: 'client/Project.html',
                descriptionClientProject: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum distinctio consequuntur, inventore ducimus delectus placeat maiores explicabo, sed quo impedit rem, nesciunt facilis id fugiat magnam aperiam a molestiae unde?'
            }
        },  
        components: {
            'app-project': project
        }   
        
    }
</script>

<style scoped>

</style>