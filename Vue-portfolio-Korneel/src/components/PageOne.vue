<template>
    <div>
        <transition name="fade" appear>
            <div class="parallax1" id="start-nav"></div>
        </transition>
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
            isHovering: false,
            }
        }
        
    }
</script>

<style scoped>
.fade-enter {
    opacity: 0;
}
.fade-enter-active {
    animation: fade-in 2s;
    transition: opacity 0.2s ;
}
@keyframes fade-in {
    from {
        transform:translateX(-30rem)
    } to {
        transform:translateX(0rem)
    }
    
}

</style>