<template>
<div class="between-wrapper" id="skill-nav">
  <h2 data-aos="fade-down" data-aos-duration="700" class="skill-title">My Skills</h2>
      <app-donut data-aos="fade-down" data-aos-duration="700"></app-donut>
        
</div>
</template>

<script>
import donutSkill from './Between-donut/donutSkill.vue'
export default {
  components: {
    'app-donut': donutSkill
  }
 
}
</script>

<style scoped>

</style>