<template>
 <div class="row">
    <div class="projects">
        <div class="imagesWork" id="css1" 
            @mouseover="isMouseOver = true"
            @mouseout="isMouseOver = false">
                <p v-show="isMouseOver">About me</p>
                <button class="work-btn button2" v-show="isMouseOver"><a href="about/index.html">Learn More</a></button>
        </div>
    </div>
    <div class="projects">
        <div class="imagesWork" id="css2"
            @mouseover="isMouseOver1 = true"
            @mouseout="isMouseOver1 = false">
                <p v-show="isMouseOver1">Grid</p>
                <button class="work-btn button2" v-show="isMouseOver1"><a href="grid/index.html">Learn More</a></button>
        </div>
    </div>
    <div class="projects">
        <div class="imagesWork"  id="css3"
            @mouseover="isMouseOver2 = true"
            @mouseout="isMouseOver2 = false">
                <p v-show="isMouseOver2">Minesweeper</p>
                <button class="work-btn button2" v-show="isMouseOver2"><a href="minesweeper/index.html">Learn More</a></button>
        </div>
    </div>
</div>
</template>

<script>

    export default {
         data: function () {
            return {
                isMouseOver: false,
                isMouseOver1: false,
                isMouseOver2: false
            }
        },     
        
    }
</script>

<style scoped>

</style>