<template>
  <div class="zr-header nav-fixed-top">
    <div class="header-container">
      <div class="header-nav">
        <router-link to="home"><span>浏览内容</span></router-link>
        <router-link to="home" class="active-link"><span>App 下载</span></router-link>
      </div>
      <h1>
        <router-link to="home">知乎日报</router-link>
      </h1>
    </div>
  </div>
</template>

<script type='text/ecmascript-6'>
  export default {
    data() {
      return {}
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
      a {
        float: right;
        @include wh(140px, 78px);
        box-sizing: border-box;
        text-decoration: none;
        & :last-child {
          margin-right: -25px;
        }
        span {
          display: block;
          margin: 23px auto 0;
          padding: 8px 0;
          width: 120px;
          font-size: 16px;
          line-height: 16px;
          text-align: center;
        }
      }
      & a:visited {
        color: #000;
      }
      .active-link span{
        background-color: #f0f9ff;
        color: #008bed;
      }
    }
  }
</style>
