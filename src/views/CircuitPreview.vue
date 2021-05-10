<template>
    <div style="overflow:auto;position: relative;">
        <div class="svg-contain">
          <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="background-color:#ffffff" viewBox="0 0 1920 1080" width="100%" height="100%">
            <defs/>
              <g
                  v-for="item in svgLists"
                  :key="item"
                  :id= item.id
                  :title=item.title
                  :transform="'translate('+(item.svgPositionX)+','+(item.svgPositionY)+')' +'rotate('+item.angle+')'"
                  :class="item.class"
              >
                <SvgComponents :height = item.height :color= item.svgColor :width= item.width :type= item.type :tableData= item.tableData :fontSize= item.fontSize :svgText= item.svgText :editable= editable></SvgComponents>
              </g>
          </svg>
        </div>
        <div class="btns-content">
          <a-button type="primary" @click="testF">退出</a-button>
        </div>
    </div>
</template>
<script>
import SvgComponents from '@/components/SvgComponents.vue';
export default {
    components: {SvgComponents},
    data(){
    return{
      svgLists:[],
      analogDataTimer:'',//模拟数据定时器
      userInfo:'',
      editable:false
  }},
  methods:{
      testF(){
        this.$router.back(-1)
      }
  },
   created(){
    let _this=this;
    _this.svgLists=JSON.parse(localStorage.getItem('svginfo'));
     console.log(localStorage.getItem('svginfo'));
   }

}
</script>
<style scoped lang="less">
.svg-contain{
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
}
.btns-content{
  position: fixed;
  left: 10px;
  bottom: 10px;
  button{
    margin-right: 10px;
  }
}
</style>
