<template>
 <div class="row">
    <div class="projects">
        <div class="imagesWork" id="html1"
            @mouseover="isMouseOver = true"
            @mouseout="isMouseOver = false">
                <p v-show="isMouseOver">HTML Basics</p>
                <button class="work-btn button2" v-show="isMouseOver"><a href="html/index.html">Learn More</a></button>
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