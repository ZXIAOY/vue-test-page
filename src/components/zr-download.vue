<template>
  <div class="zr-download">
    <div class="zr-download-content">
      <transition name="loaded-vertical">
      <div class="phone-sample-wrap" v-show="phoneSampleShow">
        <img src="../assets/image/phone_sample.png" alt="知乎日报APP" class="phone-sample">
      </div>
      </transition>
      <transition name="loaded-horizontal">
      <div class="zr-download-content-details" v-show="downloadDetailsShow">
        <h1>每天三次，每次七分钟</h1>
        <div class="info">在中国，资讯类移动应用的人均阅读时长是 5 分钟，而在知乎日报，这个数字是 21。</div>
        <div class="zr-download-qr">
          <img src="../assets/image/qr_top2.png" alt="下载二维码">
        </div>
        <div class="zr-download-link">
          <ul>
            <li><a href="https://itunes.apple.com/cn/app/id639087967?mt=8" class="iphone"><i class="icon"></i><span>iOS版</span></a></li>
            <li class="drop-menu" @mouseenter="showDownloadDrop" @mouseleave="hideDownloadDrop">
              <a href="http://zhstatic.zhihu.com/pkg/store/daily/zhihu-daily-zhihu-2.5.4(392).apk" class="android"><i class="icon"></i><span>Android版</span></a>
              <ul v-show="downloadLinkSecond">
                <li><a href="http://www.wandoujia.com/apps/com.zhihu.daily.android" class="second-menu wandoujia"><i class="icon"></i><span>豌豆荚</span></a></li>
                <li><a href="http:/zhushou.360.cn/detail/index/soft_id/348684/" class="second-menu market91"><i class="icon"></i><span>91市场</span></a></li>
                <li><a href="http://zhushou.360.cn/detail/index/soft_id/348684" class="second-menu market360"><i class="icon"></i><span>360市场</span></a></li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
      </transition>
    </div>
  </div>
</template>

<script type="text/javascript">
  import $ from 'jquery'
  export default {
    data() {
      return {
        downloadLinkSecond: false,
        downloadDetailsShow: false,
        phoneSampleShow: false
      };
    },
    mounted: function () {
      this.downloadDetailsShow = true;
      this.phoneSampleShow = true;
    },
    methods : {
      showDownloadDrop: function () {
        this.downloadLinkSecond = true;
        let dropMenuEl = document.getElementsByClassName("android");
        dropMenuEl[0].style.borderRadius = "3px 3px 0 0";
      },
      hideDownloadDrop: function () {
        this.downloadLinkSecond = false;
        let dropMenuEl = document.getElementsByClassName("android");
        dropMenuEl[0].style.borderRadius = "3px";
      },
      log: function (data) {
        console.log("zxy", data);
      }
    }
  }
</script>
<style lang="scss" type="text/scss" scoped>
  @import "../style/mixin";
  a {
    color: #39442e;
    text-decoration: none;
    outline: none;
  }
  .zr-download {
    margin-top: 78px;
    background-color: #008bed;
    z-index: 1;
    .zr-download-content {
      position: relative;
      @include horiCenter(960px);
      height: 460px;
      overflow: hidden;
      .phone-sample-wrap {
        position: absolute;
        left: 31px;
        bottom: 0;
        width: 409px;
        height: 448px;
      }
      .zr-download-content-details {
        position: absolute;
        right: 0;
        display: inline-block;
        margin-right: 22px;
        padding-top: 100px;
        width: 392px;
        text-align: left;
        h1 {
          height: 50px;
          font-size: 0;
          text-indent: -150%;
          background: transparent url("../assets/image/slogan.png") no-repeat 0 0;
        }
        .info {
          height: 100px;
          font-size: 16px;
          line-height: 26px;
          color: #99d1f8;
        }
        .zr-download-qr {
          float: left;
          @include wh(145px, 153px);
          background-color: #fff;
          border-radius: 3px;
          img {
            margin: 9px 0 0 5px;
          }
        }
        .zr-download-link {
          margin: 0 0 0 198px;
          a {
            display: block;
            height: 64px;
            background-color: #fff;
            border-radius: 3px;
            vertical-align: top;
            text-align: left;
            & i {
              display: inline-block;
              @include wh(50px, 50px);
              vertical-align: top;
              margin: 7px 0 0 5px;
            }
            span {
              display: inline-block;
              width: 108px;
              line-height: 64px;
              font-size: 22px;
              vertical-align: top;
              text-align: center;
            }
          }
          a:hover {
            background-color: #e0f3ff;
          }
          .iphone .icon {  background: transparent url("../assets/image/iphone_logo.png") 0 0;}
          .android .icon {  background: transparent url("../assets/image/android_logo.png") 0 0;}
          .wandoujia .icon {  background: transparent url("../assets/image/icon_wandoujia.png") 0 0;}
          .market91 .icon {  background: transparent url("../assets/image/icon_91market.png") 0 0;}
          .market360 .icon {  background: transparent url("../assets/image/icon_360market.png") 0 0;}
          .drop-menu {
            margin-top: 24px;
            position: relative;
             ul {
               position: absolute;
               top: 100%;
               width: 194px;
               overflow: hidden;
               a {
                 border-radius: 0px;
               }
             }
          }
        }
      }
      /*downloadDetails进入时候的过渡状态样式*/
      .loaded-horizontal-enter {         /*进入开始前*/
        opacity: 0;
        transform: translate3d(20%,0,0);
      }
      .loaded-horizontal-enter-active {  /*进入中*/
        transition: opacity 1.2s, transform 1.2s;
      }
      .loaded-horizontal-enter-to {      /*进入后*/
        opacity: 1;
        transform: translate3d(0, 0, 0);
      }
      .loaded-vertical-enter {
        opacity: 0;
        bottom: -10%;
      }
      .loaded-vertical-enter-active {
        transition: all .8s;
      }
      .loaded-vertical-enter-to {
        opacity: 1;
        bottom: 0;
      }
    }
  }
</style>
