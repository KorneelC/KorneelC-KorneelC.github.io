<template>
    <div class="column">
        <div class="donut-wrapper" v-for="(percents,i) in percent" :key='percents.skill + i'>
          <div>
            <svg viewBox="0 0 40 40" class="donut">
              <circle cx="20" cy="20" r="15.91549430918954" fill="#fff"></circle>
              <circle class="donut-ring" cx="20" cy="20" r="15.91549430918954" fill="transparent" stroke-width="3.5"></circle>
              <circle class="donut-segment" cx="20" cy="20" r="15.91549430918954" fill="transparent" stroke-width="3.5" :stroke-dasharray="[percents.perc,100 - percents.perc]" stroke-dashoffset="25"></circle>
              <g class="donut-text">
              <text y="50%" transform="translate(0, 2)">
                <tspan x="50%" text-anchor="middle" class="donut-percent">{{percents.perc}}%</tspan>   
              </text>
              <text y="60%" transform="translate(0, 2)">
                <tspan x="50%" text-anchor="middle" class="donut-data">{{percents.skill}}</tspan>   
              </text>
              </g>
            </svg>
          </div>
          <p>{{percents.skill}}</p>
        </div>
</div>
</template>

<script>

 
export default {
  data: function() {
      return {
          percent: [
            {skill:'HTML', perc:90},
            {skill:'CSS', perc: 78},
            {skill:'SCSS', perc: 71},
            {skill:'JAVASCRIPT', perc: 80},
            {skill:'Vue.js', perc:60}
            ]
      }
  },
}
</script>

<style scoped>




</style>