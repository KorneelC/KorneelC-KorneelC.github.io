<template>
 <div class="row">
    <div class="projects">
        <div class="imagesWork" id="vue1"
            @mouseover="isMouseOver = true"
            @mouseout="isMouseOver = false">
                <p v-show="isMouseOver">Portfolio</p>
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