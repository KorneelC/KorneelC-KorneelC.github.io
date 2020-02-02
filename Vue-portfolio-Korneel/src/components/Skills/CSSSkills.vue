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
        <div :class="{'description':isTextvisible,'css3':defaultText,
        imagesWork:defaultText}"
            @mouseover="isMouseOver2 = true"
            @mouseleave="showImage">
                <p v-if="isTextvisible == false" v-show="isMouseOver2">Minesweeper</p>
                <button v-if="isTextvisible == false" class="work-btn button2" v-show="isMouseOver2" @click="showText">Learn more</button>
                <div v-else>
                    <p> Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laboriosam quo deleniti quam voluptas eius id eos cumque! Similique id tempore veniam odit voluptatum veritatis velit est distinctio molestias, animi unde?</p>
                    <div class="btnDescription">
                        <button class="work-btn button2"><a href="minesweeper/index.html">Result</a></button>
                        <button @click="showImage" class="work-btn button2">Go back</button>
                    </div>
                </div>
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
                isMouseOver2: false,
                isTextvisible: false,
                defaultText: true
            }
        },
        methods: {
            showText () {
                this.isTextvisible = true
                this.defaultText = false
            },
            showImage () {
                this.isTextvisible = false
                this.defaultText = true
                this.isMouseOver2 = false
            }
        }     
        
    }
</script>

<style scoped>

</style>