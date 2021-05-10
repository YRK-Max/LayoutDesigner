<template>
  <rect :x="-(height/2)" :y="-(height/2)" :width="height" :height="height" :fill="color" :stroke="strokeColor" :stroke-width="width" ></rect>
  <line fill="none" :stroke="strokeColor" :stroke-width="width" :x1="-(height/2)" :x2="-(height/2) + (height)" :y1="-(height/2)" :y2="-(height/2) + (height)"/>
  <line fill="none" :stroke="strokeColor" :stroke-width="width" :x1="-(height/2) + (height)" :x2="-(height/2)" :y1="-(height/2)" :y2="-(height/2) + (height)"/>
  <text :x="-height/2.5" :y="(height/2) + 20" :font-size="fontSize">{{ text }}</text>
</template>

<script>
export default {
  name: "Port",
  props: ['height', 'color', 'width', 'strokeColor', 'text', 'fontSize']
}
</script>

<style scoped>

</style>
