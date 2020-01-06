<template>
 <div class="row">
    <div class="projects">
        <div class="imagesWork" id="scss1"
            @mouseover="isMouseOver = true"
            @mouseout="isMouseOver = false">
                <p v-show="isMouseOver">Mobile version</p>
                <button class="work-btn button2" v-show="isMouseOver"><a href="admin/index.html">Learn More</a></button>
        </div>
    </div>
    <div class="projects">
        <div class="imagesWork" id="scss2"
            @mouseover="isMouseOver1 = true"
            @mouseout="isMouseOver1 = false">
                <p v-show="isMouseOver1">Multipage</p>
                <button class="work-btn button2" v-show="isMouseOver1"><a href="multipage/korneel.html">Learn More</a></button>
        </div>
    </div>
    <div class="projects">
        <div class="imagesWork" id="scss3"
            @mouseover="isMouseOver2 = true"
            @mouseout="isMouseOver2 = false">
                <p v-show="isMouseOver2">Client Project</p>
                <button class="work-btn button2" v-show="isMouseOver2"><a href="client/Project.html">Learn More</a></button>
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