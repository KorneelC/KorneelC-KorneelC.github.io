<template>
 <div class="row">
    <div class="projects">
        <div class="imagesWork" id="js1"
            @mouseover="isMouseOver = true"
            @mouseout="isMouseOver = false">
                <p v-show="isMouseOver">Snake</p>
                <button class="work-btn button2" v-show="isMouseOver"><a href="snake/index.html">Learn More</a></button>
        </div>
    </div>
    <div class="projects">
        <div class="imagesWork" id="js2"
            @mouseover="isMouseOver1 = true"
            @mouseout="isMouseOver1 = false">
                <p v-show="isMouseOver1">RPG</p>
                <button class="work-btn button2" v-show="isMouseOver1"><a href="rpg/index.html">Learn More</a></button>
        </div>
    </div>
    <div class="projects">
        <div class="imagesWork" id="js3"
            @mouseover="isMouseOver2 = true"
            @mouseout="isMouseOver2 = false">
                <p v-show="isMouseOver2">Forms</p>
                <button class="work-btn button2" v-show="isMouseOver2"><a href="form/index.html">Learn More</a></button>
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