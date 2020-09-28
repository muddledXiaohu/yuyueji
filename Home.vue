<template>
    <div class="bgis">
      <img
      class="clasBgiO"
      src="../assets/clasBgi.png"
      border="0" usemap="#planetmap"
      alt="Planets" />

      <map name="planetmap" id="planetmap">
        <!-- top的刷新 -->
        <area shape="circle" coords="1025,120,44" @click="displayO" />
        <!-- 打开12个按钮 -->
        <area shape="circle" coords="1023,277,75" @click="displays" />
        <area shape="circle" coords="1025,1267,73" @click="qwe" />
        <area shape="circle" coords="1025,1431,55" @click="qwe" />
        <area shape="circle" coords="348,771,48" @click="qwe" />
        <area shape="circle" coords="527,773,72" @click="introduction" />
          <!-- 楼层简介按钮 -->
        <area shape="circle" coords="1523,777,74" @click="qwe" />
        <area shape="circle" coords="1698,774,45" @click="qwe" />

        <!-- 预约登录 -->
        <area shape="rect" coords="891,713,1168,782" @click="qwe" />
        <area shape="rect" coords="889,854,1169,922" @click="qwe" />
      </map>

      <img
      class="clasBgiT"
      style="display:none;"
      src="../assets/clasBgiTwo.png"
      border="0" usemap="#BgiTwo"
      alt="Planets" />

      <map name="BgiTwo" id="BgiTwo">
        <!-- top的刷新 -->
        <area shape="circle" coords="1025,120,44" @click="displayO" />
        <!-- 打开12个按钮 -->
        <area shape="circle" coords="1023,277,75" @click="displays" />
        <area shape="circle" coords="1025,1267,73" @click="qwe" />
        <area shape="circle" coords="1025,1431,55" @click="qwe" />
        <area shape="circle" coords="348,771,48" @click="qwe" />
        <area shape="circle" coords="527,773,72" @click="introduction" />
          <!-- 楼层简介按钮 -->
        <area shape="circle" coords="1523,777,74" @click="qwe" />
        <area shape="circle" coords="1698,774,45" @click="qwe" />

        <!-- 12个按钮 -->
        <area shape="circle" coords="1218,310,45" @click="qwe" />
        <area shape="circle" coords="1378,418,47" @click="qwe" />
        <area shape="circle" coords="1485,579,44" @click="qwe" />
        <area shape="circle" coords="1485,960,43" @click="qwe" />
        <area shape="circle" coords="1376,1121,44" @click="qwe" />
        <area shape="circle" coords="1215,1229,43" @click="qwe" />
        <area shape="circle" coords="833,1228,43" @click="qwe" />
        <area shape="circle" coords="672,1120,47" @click="qwe" />
        <area shape="circle" coords="567,957,44" @click="qwe" />
        <area shape="circle" coords="565,577,46" @click="qwe" />
        <area shape="circle" coords="673,417,47" @click="qwe" />
        <area shape="circle" coords="837,309,43" @click="qwe" />

        <!-- 预约登录 -->
        <area shape="rect" coords="891,713,1168,782" @click="qwe" />
        <area shape="rect" coords="889,854,1169,922" @click="qwe" />

      </map>

      <!-- 楼层简介 -->
        <img
        class="clasBgiTh"
        style="display:none;"
        src="../assets/base.png"
        border="0" usemap="#briefInt"
        alt="Planets" />
        <map name="briefInt" id="briefInt">
          <!-- top的刷新 -->
          <area shape="circle" coords="1025,120,44" @click="displayO" />
          <!-- 打开12个按钮 -->
          <area shape="circle" coords="1023,277,75" @click="displays" />
          <area shape="circle" coords="1025,1267,73" @click="qwe" />
          <area shape="circle" coords="1025,1431,55" @click="qwe" />
          <area shape="circle" coords="348,771,48" @click="qwe" />
          <area shape="circle" coords="527,773,72" @click="introduction" />
          <!-- 楼层简介按钮 -->
          <area shape="circle" coords="1523,777,74" @click="qwe" />
          <area shape="circle" coords="1698,774,45" @click="qwe" />

          <!-- 12个按钮 -->
          <area shape="circle" coords="1218,310,45" @click="qwe" />
          <area shape="circle" coords="1378,418,47" @click="qwe" />
          <area shape="circle" coords="1485,579,44" @click="qwe" />
          <area shape="circle" coords="1485,960,43" @click="qwe" />
          <area shape="circle" coords="1376,1121,44" @click="qwe" />
          <area shape="circle" coords="1215,1229,43" @click="qwe" />
          <area shape="circle" coords="833,1228,43" @click="qwe" />
          <area shape="circle" coords="672,1120,47" @click="qwe" />
          <area shape="circle" coords="567,957,44" @click="qwe" />
          <area shape="circle" coords="565,577,46" @click="qwe" />
          <area shape="circle" coords="673,417,47" @click="qwe" />
          <area shape="circle" coords="837,309,43" @click="qwe" />

          <!-- 导航一到四楼 -->
          <area shape="rect" coords="894,580,1149,633" @click="masks" />
          <area shape="rect" coords="896,689,1153,738" @click="masks" />
          <area shape="rect" coords="899,795,1148,846" @click="masks" />
          <area shape="rect" coords="898,899,1150,954" @click="masks" />
        </map>

        <!-- 遮罩层 -->
        <div class="zzc">
          <el-carousel :interval="4000" type="card" height="200px">
            <el-carousel-item v-for="item in 6" :key="item">
            </el-carousel-item>
          </el-carousel>
        </div>
    </div>
</template>

<script>
import $ from 'jquery'
export default {
  data () {
    return {
    }
  },
  created () {

  },
  methods: {
    qwe () {
      console.log(1)
    },
    displays () {
      $('.clasBgiT').fadeToggle(2000)
    },

    // 刷新显示
    displayO () {
      $('.clasBgiT').fadeOut(300).fadeIn(2000)
    },

    // 基地楼层简介
    introduction () {
      $('.clasBgiTh').fadeToggle(3)
    },

    // 遮罩层图片显示
    masks () {

    }
  }
}
</script>
<style lang="less" scoped>
  .clasBgiT{
    position: absolute;
    top: 0;
    left: 0;
  }
  .clasBgiO{
    position: absolute;
    top: 0;
    left: 0;
  }
  .clasBgiTh{
    position: absolute;
    top: 0;
    left: 0;
  }
  // 遮罩层
    .zzc{
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(0, 0, 0, 0.5);
    }
    .el-carousel{
      // display: none;
      position: absolute;
      width: 80%;
      top: 10%;
      left: 50%;
      transform: translateX(-50%);
    }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
  /deep/.el-carousel__container {
    height: 600px!important;
  }
  /dee/.el-carousel__indicators--outside {
    position: absolute!important;
    bottom: 5%;
  }
  /deep/.el-carousel__item--card {
    width: 70%;
  }
  /deep/.el-carousel__item, .el-carousel__mask {
    left: -10%;
  }
</style>
