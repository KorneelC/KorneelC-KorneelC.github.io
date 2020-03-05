<template>
 <div class="row">
     <app-project :titleId="vue1" :title="titleVueProject" :descriptionWork="descriptionVueProject"></app-project>
 </div>
  
</template>

<script>
    import project from './project.vue'
    export default {
        data () {
          return {
                vue1: 'portfolio',
                titleVueProject:'My portfolio',
                descriptionVueProject: 'This portfolio is made in Vue.js'
            }
        }, 
        components:  {
            'app-project': project
        }   
        
    }
</script>

<style scoped>

</style>