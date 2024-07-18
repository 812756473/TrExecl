<template>
  <div id="luckysheet" style="margin:0px;padding:0px;width:100%;height:100%;"></div>
</template>

<script setup>
import { onMounted } from 'vue'

const init = ()=>{
   var options = {
    title:'',
    showinfobar:false,
    enableAddRow:false,
    enableAddBackTop:false,
    data:[
      {
        "name": "sheet1", //工作表名称
        "celldata": [
          {"r":0,"c":0,"v":{"v":6656,"ct":{"fa":"General","t":"n"}}},
          {"r":0,"c":1,"v":{"fc":"rgb(51,68,222)","v":"sasa",}},
        ], //初始化使用的单元格数据
      },
      {
        "name": "sheet2", //工作表名称
        "celldata": [
          {"r":0,"c":0,"v":{"v":1}},
          {"r":0,"c":1,"v":{"v":2}},
          {"r":10,"c":10,"v":{"v":'测试',"fc":"rgb(51,68,222)"}},
        ], //初始化使用的单元格数据
      },
    ],
    showtoolbarConfig:{
			print: false,
		},
    showsheetbarConfig:{
      add: true, //新增sheet  
      menu: false, //sheet管理菜单
      sheet: true //sheet页显示
    },
    showstatisticBarConfig:{
      count: false, // 计数栏
      view: false, // 打印视图
      zoom: false, // 缩放
    },
    
    container: 'luckysheet', //luckysheet为容器id
    lang: 'zh' 
  }
  luckysheet.create(options)
}

onMounted(()=>{
  init()
})
</script>

<style lang="scss" scoped>

</style>