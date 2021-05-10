<!-- 箭头向下svg组件 -->
<template>
  <Cleaner :height = height :color= color :stroke-color="strokeColor" :width= width :text="svgText" :font-size="fontSize" v-if="type==='CleanerSvg'"></Cleaner>
  <port :height = height :color= color :stroke-color="strokeColor" :width= width v-else-if="type==='PortSvg'"></port>
  <Cut :height = height :color= color :stroke-color="strokeColor" :width= width :text="svgText" :font-size="fontSize" v-else-if="type==='CutSvg'"></Cut>
</template>
<script>
import Cleaner from "@/components/svgCpt/Cleaner";
import Port from "@/components/svgCpt/Port";
import Cut from "@/components/svgCpt/Cut";
//发电站
export default {
    props: ['height','color','width','type','fontSize','tableData','svgText','editable', 'strokeColor'],
    components: {
      Cut,
      Port,
      Cleaner
    },
};
</script>
