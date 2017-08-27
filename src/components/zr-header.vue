<template>
  <header class="zr-header nav-fixed-top">
    <div class="header-container">
      <div class="header-nav">
        <span @click="viewContent" class="view-content">浏览内容</span>
        <span @click="viewDownload" class="active-link view-app-download">App 下载</span>
      </div>
      <h1>
        <router-link to="home">知乎日报</router-link>
      </h1>
    </div>
  </header>
</template>

<script type='text/ecmascript-6'>

  export default {
    data() {
      return {}
    },
    methods: {
      viewContent: function () {
        console.log("点击");
        window.scrollTo(0,470);
      },
      viewDownload: function () {
        window.scrollTo(0,78);
      }
    }
  }
</script>

<style type="text/scss" lang="scss">
  @import "../style/mixin";

  .zr-header.nav-fixed-top{
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 999;
    height: 78px;
    box-sizing: border-box;
    background-color: #fff;
  }
  .header-container {
    @include horiCenter(960px);
    cursor: pointer;
    h1 {
      width: 220px;
      background: transparent url("../assets/image/top_logo.png") no-repeat 0 13px;
      a {
        display: block;
        height: 78px;
        font-size: 0;
        text-indent: -150%;
      }
    }
    .header-nav {
      float: right;
      margin-right: -24px;
      span {
        float: right;
        display: block;
        box-sizing: border-box;
        margin: 23px auto 0;
        padding: 8px 0;
        width: 120px;
        font-size: 16px;
        line-height: 16px;
        text-align: center;
        & :last-child {
          margin-right: -25px;
        }
      }
      & span:visited {
        color: #000;
      }
      .active-link{
        background-color: #f0f9ff;
        color: #008bed;
      }
    }
  }
</style>
