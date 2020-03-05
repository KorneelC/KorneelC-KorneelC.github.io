<template>
    <div :class="{'description':isTextvisible, 'imagesWork':defaultText}" :style="{backgroundImage: defaultText? 'linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),url('+require('../../resources/images/' + titleId + '.png')+')': ''}"
        @mouseover="isMouseOver = true"
        @mouseleave="showImage">
        <p v-if="defaultText" v-show="isMouseOver">{{title}}</p>
        <button v-if="defaultText" class="work-btn button2" v-show="isMouseOver" @click="showText">Learn more</button>
        <div v-else>
            <p>{{descriptionWork}}</p>
            <div class="btnDescription">
                <button class="work-btn button2"><a :href="link">Result</a></button>
                <button @click="showImage" class="work-btn button2">Go back</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        title: String,
        titleId: String,
        descriptionWork: String,
        link: String
        },
      data () {
            return {
                isMouseOver: false,
                isTextvisible: false,
                defaultText: true,
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
                this.isMouseOver = false
            }
        }
};
</script>

<style scoped>

</style>