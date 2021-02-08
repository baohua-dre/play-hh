<template>
  <div>
    <dv-full-screen-container style="background:#0C1A30;">
      <div  class="header">
        <dv-decoration-8 style="width:300px;height:50px;" />
        <div class="titleCon">
          <dv-decoration-7 :color="['#3F96A5']" style="width:150px;height:30px;" class="dataSty"> 可视化DataV </dv-decoration-7>
          <dv-decoration-5 style="width:300px;height:40px;" />
        </div>
        <dv-decoration-8 :reverse="true" style="width:300px;height:50px;" />
      </div>
      <dv-decoration-10 style="width:90%;height:5px;" class="deco"/>
      <dv-border-box-1 style="height:450px;">
        <div class="bigcontainer">
            <div class="conLeft">
              <dv-scroll-ranking-board :config="config" style="width:300px;height:400px; " />
            </div>
            <div class="picContainer">
              <dv-border-box-12 >
                <dv-flyline-chart-enhanced :config="configPhoto" style="width:100%;height:100%;" />
              </dv-border-box-12>
            </div>
            <div class="conRight">
              <div style="padding:20px;display:flex;align-content:flex-start;flex-wrap:wrap;">
                <dv-water-level-pond :config="waterConfi" style="width:100px;height:150px" />
                <dv-active-ring-chart :config="confighuan" style="width:200px;height:200px" />
                <dv-decoration-9 style="width:150px;height:150px;">66%</dv-decoration-9>
                <dv-decoration-12 style="width:150px;height:150px;" />
              </div>
            </div>
        </div>
      </dv-border-box-1>
    </dv-full-screen-container>
    
  </div>
</template>
 
<script>
export default {
  name: "About",
  data () {
    return {
      msg:'Welcome to your vueName',
      // 轮播表
      config:{
        data: [
          {
            name: '周口',
            value: 55
          },
          {
            name: '南阳',
            value: 120
          },
          {
            name: '西峡',
            value: 78
          },
          {
            name: '驻马店',
            value: 66
          },
          {
            name: '新乡',
            value: 80
          },
          {
            name: '信阳',
            value: 45
          },
          {
            name: '漯河',
            value: 29
          }
        ]
      },
      // 水位图
      waterConfi:{
        data: [66, 45],
        shape: 'roundRect'
      },
      // 飞线图
      configPhoto:{
         points: [
          {
            name: '郑州',
            coordinate: [0.48, 0.35]
          },
          {
            name: '新乡',
            coordinate: [0.52, 0.23]
          },
          {
            name: '焦作',
            coordinate: [0.43, 0.29]
          },
          {
            name: '开封',
            coordinate: [0.59, 0.35]
          },
          {
            name: '许昌',
            coordinate: [0.53, 0.47]
          },
          {
            name: '平顶山',
            coordinate: [0.45, 0.54]
          },
          {
            name: '洛阳',
            coordinate: [0.36, 0.38]
          },
          {
            name: '周口',
            coordinate: [0.62, 0.55]
          },
          {
            name: '漯河',
            coordinate: [0.56, 0.56]
          },
          {
            name: '南阳',
            coordinate: [0.37, 0.66]
          },
          {
            name: '信阳',
            coordinate: [0.55, 0.81]
          },
          {
            name: '驻马店',
            coordinate: [0.55, 0.67]
          },
          {
            name: '济源',
            coordinate: [0.37, 0.29]
          },
          {
            name: '三门峡',
            coordinate: [0.20, 0.36]
          },
          {
            name: '商丘',
            coordinate: [0.76, 0.41]
          },
          {
            name: '鹤壁',
            coordinate: [0.59, 0.18]
          },
          {
            name: '濮阳',
            coordinate: [0.68, 0.17]
          },
          {
            name: '安阳',
            coordinate: [0.59, 0.10]
          }
        ],
        lines: [
          {
            source: '新乡',
            target: '郑州'
          },
          {
            source: '焦作',
            target: '郑州'
          },
          {
            source: '开封',
            target: '郑州'
          },
          {
            source: '许昌',
            target: '郑州'
          },
          {
            source: '平顶山',
            target: '郑州'
          },
          {
            source: '洛阳',
            target: '郑州'
          },
          {
            source: '周口',
            target: '郑州'
          },
          {
            source: '漯河',
            target: '郑州'
          },
          {
            source: '南阳',
            target: '郑州'
          },
          {
            source: '信阳',
            target: '郑州'
          },
          {
            source: '驻马店',
            target: '郑州'
          },
          {
            source: '济源',
            target: '郑州'
          },
          {
            source: '三门峡',
            target: '郑州'
          },
          {
            source: '商丘',
            target: '郑州'
          },
          {
            source: '鹤壁',
            target: '郑州'
          },
          {
            source: '濮阳',
            target: '郑州'
          },
          {
            source: '安阳',
            target: '郑州'
          }
        ],
        bgImgSrc: './img/map.jpg'
      },
      // 动态环图
      confighuan:{
        data: [
          {
            name: '周口',
            value: 55
          },
          {
            name: '南阳',
            value: 120
          },
          {
            name: '西峡',
            value: 78
          },
          {
            name: '驻马店',
            value: 66
          },
          {
            name: '新乡',
            value: 80
          }
        ],
        lineWidth: 10,
        digitalFlopStyle: {
          fontSize: 14,
          fill: '#fff'
        }
      }
    }
  },
  created() { },
  // mounted:{ },
  methods: { },
}
</script>
 
<style scoped lang='scss'>
  .header {
    height: 100px;
    display: flex;
    padding-top: 20px;
    align-content: space-around;
  }

  .dataSty {
    color: #ccc;
    font-size: 20px;
    margin: 0 auto;
  }
  .titleCon {
    margin: 0 270px;
  }
  .deco{
    margin: -20px auto 20px auto;
    
    // margin: -10px 0 10px 0;
  }
  .bigcontainer {
    display: flex;
    align-content: space-around;
    margin:20px;
    .conLeft {
      width: 25%;
      margin: 20px;
    }
    .picContainer{
      width: 50%;
    }
    .conRight{
      width: 25%;
    }
  }
</style>