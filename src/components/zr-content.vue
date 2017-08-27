<template>
    <div class="zr-content">
      <div class="zr-content-wrap">
        <div class="content-head">
          <div class="head-tip">最新内容</div>
          <div class="head-title">浏览内容</div>
        </div>
        <div class="content-body">
          <zr-item class="zr-item" v-for="item in zrItemsData" :key="item.picSrc" :item-title="item.title" :item-src="item.picSrc"></zr-item>
        </div>
        <a href="#" class="read-more">更多精彩内容可在知乎日报应用中查看</a>

      </div>
    </div>
</template>

<script type='text/ecmascript-6'>
    import zrItem from "./zr-item.vue"
    export default {
      data () {
        return {
          zrItemsData: [
            { picSrc: "https://pic3.zhimg.com/v2-b6052721784024ea3725cacf41da948e.jpg" ,
              title: "你所在的领域，有哪些曾经流传甚广，但最后被证明是错误的东西"},
            { picSrc: "https://pic4.zhimg.com/v2-1fdd2ea58f71b1141a8aabf3e6d530b3.jpg",
              title: "做好孩子的陪玩教练，离不开这四个关键词"},
            { picSrc: "https://pic4.zhimg.com/v2-6de32b4eff9fcdf1778f7aa1a0330103.jpg",
              title: "养布偶猫是种怎样的体验？"},
            { picSrc: "https://pic3.zhimg.com/v2-b6052721784024ea3725cacf41da948e.jpg" ,
              title: "33 天孤身穿越中国最大的无人区，他成就了一个人的史诗"},
            { picSrc: "https://pic4.zhimg.com/v2-1fdd2ea58f71b1141a8aabf3e6d530b3.jpg",
              title: "做好孩子的陪玩教练，离不开这四个关键词"},
            { picSrc: "https://pic4.zhimg.com/v2-6de32b4eff9fcdf1778f7aa1a0330103.jpg",
              title: "你所在的领域，有哪些曾经流传甚广，但最后被证明是错误的东西"},
            { picSrc: "https://pic3.zhimg.com/v2-b6052721784024ea3725cacf41da948e.jpg" ,
              title: "你所在的领域，有哪些曾经流传甚广，但最后被证明是错误的东西"},
            { picSrc: "https://pic4.zhimg.com/v2-1fdd2ea58f71b1141a8aabf3e6d530b3.jpg",
              title: "做好孩子的陪玩教练，离不开这四个关键词"},
            { picSrc: "https://pic4.zhimg.com/v2-6de32b4eff9fcdf1778f7aa1a0330103.jpg",
              title: "养布偶猫是种怎样的体验？"}]
        }
      },
      components: {
        "zr-item": zrItem,
      }

    }
</script>

<style type="text/scss" lang="scss">
  .zr-content {
    margin-bottom: 30px;
    background-color: #f9f9f9;
    .zr-content-wrap {
      margin: 0 auto;
      width: 960px;
      //头部标题
      .content-head {
        padding: 44px 0 31px;
        font-size: 25px;
        .head-tip {
          float: right;
          line-height: 25px;
          color: #ccc;
        }
        .head-title {
          line-height: 25px;
        }
      }
      //内容主体
      .content-body {
        display: flex;
        flex-flow: row wrap;
        justify-content: space-between;
        align-content: flex-start;
        .zr-item {

          flex: 1 1 260px;
        }
      }
      //底部标签
      .read-more {
        display: block;
        height: 62px;
        line-height: 62px;
        font-size: 20px;
        text-align: center;
        color: #15527b;
        text-decoration: none;
        background-color: #e8eef2;
        border-radius: 3px;
      }

    }
  }
</style>
