<template>
    <div class="none">
        <div class="parallax1" id="start-nav"></div>
        <div class="content">
            <h2>Hello, I'm <span class="name">Korneel</span>.<span class="title-d">I'm a junior web developer trained by <a id="becode" href="https://www.becode.org/register/register_nl.html">BeCode</a> Genk.</span></h2>
            <button
              href="#skills-nav"
             @mouseover="isHovering = true" 
             @mouseout="isHovering = false" 
             class="work-btn"><a href="#work-nav">View my work 
             <i :class="{
                'fas fa-arrow-left': !isHovering,
                'fas fa-arrow-down': isHovering
             }"
            ></i></a></button>
        </div>
    </div>
</template>

<script>
    export default {
        data () {
            return {
            isHovering: false
            }
        }
        
    }
</script>

<style scoped>


</style>