<template>
  <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
  :width="width" viewBox="0 0 559.357 99.271" enable-background="new 0 0 559.357 99.271" x="0px" y="0px">
<g>
  <polygon class="red"  points="0.225,15.276 18.838,21.77 18.979,99.271 0,92.715  "/>
<g class="purple">
  <polygon   points="45.715,0 61.296,5.201 61.422,67.255 45.534,62.003   "/>
  <polygon   points="23.458,6.212 41.984,13.95 42.167,81.392 23.18,73.098  "/>
  <polygon   points="66.751,10.326 80.059,14.321 80.183,61.937 66.613,57.902   "/>
</g>
</g>
<text transform="matrix(1 0 0 1 103.5298 64.0322)">
  <tspan class="purple" x="0" y="0" fill="#262262" font-family="'Work sans'" font-size="72">Instant</tspan>
  <tspan x="227.013" y="0" fill="#92278F" font-family="'MyriadPro-Bold'" font-size="72"></tspan>
  <tspan x="260.1" y="0" class="red" font-family="'Work sans'" font-size="72">P</tspan>
  <tspan class="purple" x="297.932" y="0" fill="#262262" font-family="'Work sans'" font-size="72">ower</tspan>
</text>
</svg>
   <!-- <img src="https://instantpower.ng/logo-full.png" class="logo"> -->
</template>

<script>
  
export default {
   name: 'logo',
   props: {
     width: {
        default: '150px'

     },

     height: {
        default: '50px'
     }
   }
}

</script>

<style>
.purple {
   fill: #262262;
}

.red {
   fill: #BE1E2D;
}

.purple:hover {
   fill: #BE1E2D;
}

.red:hover {
   
   fill: #262262;
}

.logo {
   max-width: 150px;
   height: auto;
}


</style>
