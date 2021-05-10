<template>
  <rect :x="-(height/2)" :y="-(height/2)" :width="height" :height="height/4" :fill="color" :stroke="strokeColor || '#000000'" :stroke-width="width" ></rect>
  <rect :x="-(height/2)" :y="-(height/2) + (height/4)" :width="height" :height="height/4" :fill="color" :stroke="strokeColor || '#000000'" :stroke-width="width" ></rect>
  <rect :x="-(height/2)" :y="-(height/2) + 2*(height/4)" :width="height" :height="height/4" :fill="color" :stroke="strokeColor || '#000000'" :stroke-width="width" ></rect>
  <rect :x="-(height/2)" :y="-(height/2) + 3*(height/4)" :width="height" :height="height/4" :fill="color" :stroke="strokeColor || '#000000'" :stroke-width="width" ></rect>
  <circle :cx="(height/64)" :cy="0" :fill="color" :stroke="strokeColor || '#000000'" :stroke-width="width"  :r="(height/3.5)"></circle>
  <text :x="-height/8" :y="(height/2) + 20" :font-size="fontSize">{{ text }}</text>
</template>

<script>
export default {
  name: "Cleaner",
  props: ['height','color','width', 'text', 'fontSize', 'strokeColor']
}
</script>

<style scoped>

</style>
