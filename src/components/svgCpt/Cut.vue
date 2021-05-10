<template>
  <rect :x="-(height/2)" :y="-(height/2)" :width="height/4" :height="height" :fill="color" :stroke="strokeColor" :stroke-width="width" ></rect>
  <rect :x="-(height/8)" :y="-(height/4)" :width="height/2" :height="height/2" :fill="color" :stroke="strokeColor" :stroke-width="width" ></rect>
  <circle :cx="(height/8)" :cy="0" :fill="color" :stroke="strokeColor" :stroke-width="width"  :r="(height/3.5)"></circle>
  <rect :x="-(height/125)" :y="-(height/10)" :width="height/4" :height="height/5" :fill="color" :stroke="strokeColor" :stroke-width="width" ></rect>
  <rect :x="(height/2)" :y="-(height/2)" :width="height/4" :height="height" :fill="color" :stroke="strokeColor" :stroke-width="width" ></rect>
  <text :x="0" :y="(height/2) + 20" :font-size="fontSize">{{ text }}</text>
</template>

<script>
export default {
  name: "Cut",
  props: ['height','color','width', 'text', 'fontSize', 'strokeColor']
}
</script>

<style scoped>

</style>
