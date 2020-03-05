<template>
    <div class="row">
        <app-project :titleId="css1" :title="titleAboutMe" :link="linkAboutMe" :descriptionWork="descriptionAboutMeProject"></app-project>
        <app-project :titleId="css2" :title="titleGrid" :link="linkGrid" :descriptionWork="descriptionGridProject"></app-project>
        <app-project :titleId="css3" :title="titleMinesweeper" :link="linkMinesweeper" :descriptionWork="descriptionMinesweeperProject"></app-project>
    </div>

</template>

<script>
    import project from './project.vue'
    export default {
         data: function () {
            return {
                css1: 'about',
                css2: 'chessboard',
                css3 : 'minesweeper',
                titleAboutMe:'About me',
                titleGrid: 'Grid',
                titleMinesweeper: 'Minesweeper',
                linkAboutMe: 'about/index.html',
                linkGrid: 'grid/index.html',
                linkMinesweeper: 'minesweeper/index.html',
                descriptionAboutMeProject: 'In this project I used flexbox to make this website where I described myself.',
                descriptionGridProject: 'This is the exercise where I learned to use grid. You can play this game if you use your inspector!',
                descriptionMinesweeperProject: 'In this excersise I used CSS3 to apply some colours/effects to this home-made minesweeper. Be aware it is not functional'

            }
        },
        components: {
            'app-project': project
        }
        
    }
</script>

<style scoped>

</style>