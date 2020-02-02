<template>
  <div class="projects">
        <div :class="{titleId:defaultText,'description':isTextvisible, 'imagesWork':defaultText}" :style="{'background-image': `url(${(titleId)})`} "
            @mouseover="isMouseOver = true"
            @mouseleave="showImage">
                <p v-if="isTextvisible == false" v-show="isMouseOver">{{title}}</p>
                <button v-if="isTextvisible == false" class="work-btn button2" v-show="isMouseOver" @click="showText">Learn more</button>
                <div v-else>
                    <p>{{descriptionWork}}</p>
                    <div class="btnDescription">
                        <button class="work-btn button2"><a :href="link">Result</a></button>
                        <button @click="showImage" class="work-btn button2">Go back</button>
                    </div>
                </div>
        </div>
        <p>{{titleId}}</p>
    </div>
</template>

<script>
export default {
    name:'project',
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