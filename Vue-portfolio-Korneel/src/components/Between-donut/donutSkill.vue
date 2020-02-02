<template>
    <div class="column">
        <div class="donut-wrapper" v-for="percents in percent" :key='percents'>
          <div class="svg-item">
            <svg viewBox="0 0 40 40" class="donut">
              <circle class="donut-hole" cx="20" cy="20" r="15.91549430918954" fill="#fff"></circle>
              <circle class="donut-ring" cx="20" cy="20" r="15.91549430918954" fill="transparent" stroke-width="3.5"></circle>
              <circle class="donut-segment donut-segment-2" cx="20" cy="20" r="15.91549430918954" fill="transparent" stroke-width="3.5" :stroke-dasharray="[percents.perc,100 - percents.perc]" stroke-dashoffset="25"></circle>
              <g class="donut-text donut-text-1">
              
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
          percent: [{skill:'HTML', perc:90}, {skill:'CSS', perc: 78}, {skill:'SCSS', perc: 71},{skill:'JAVASCRIPT', perc: 80},{ skill:'Vue.js', perc:60}]
      }
  },
}
</script>

<style scoped>

.donut {
    width: 10rem;
    height: 10rem;
}

.donut-ring {
    stroke: #EBEBEB;
}


.donut-segment-2 {
    stroke: #19ebeb;
    animation: donut1 3s; 
}

@keyframes donut1 {
    0% {
        stroke-dasharray: 0, 100;
    }
}


.donut-text {
    font-family: Arial, Helvetica, sans-serif;
}
.donut-text-1 {
    fill: #19ebeb;
}

.donut-percent {
    font-size: 0.5rem;
    line-height: 1;
    transform: translateY(0.5rem);
    font-weight: bold;
}

.donut-data {
    font-size: 0.12rem;
    line-height: 1;
    transform: translateY(0.5em);
    text-align: center;
    text-anchor: middle;
    color:rgb(2, 51, 54);
    fill:rgb(2, 51, 54);
}


</style>