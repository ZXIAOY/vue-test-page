<template>
    <footer class="zr-footer">
      <div class="zr-footer-wrap">
        <div class="footer-qr">
          <div class="footer-qr-wrap">
            <img src="../assets/image/qr_bottom.png" alt="">
          </div>
          <p>扫描下载客户端</p>
        </div>
        <div class="footer-info">
          <p>知乎日报是一款拥有千万用户的资讯类客户端，每日提供来自知乎社区的精选问答，还有国内一流媒体的专栏特稿。</p>
          <p>主题日报包括动漫、设计、大公司、游戏、财经、电影、电子音乐、互联网安全等丰富内容，为业内人和资深爱好<br>
            者推荐各领域最精彩文章，满足高质量阅读需求。</p>
          <p>在知乎日报，告别浮躁，重获阅读的愉悦。</p>
          <p>&copy;模仿知乎_zty</p>
        </div>
      </div>
    </footer>
</template>

<script type='text/ecmascript-6'>
    export default {

    }
</script>

<style type="text/scss" lang="scss">
  .zr-footer {
    margin-top: 20px;
    background-color: #e5e5e5;
    color: #666;
    .zr-footer-wrap {
      padding-bottom: 60px;
      width: 960px;
      margin: 0 auto;
      .footer-qr {
        float: right;
        padding-top: 25px;
        .footer-qr-wrap {
          background-color: #fff;
          padding: 6px 4px;
          border-radius: 4px;
        }
        p {
          margin-top: 12px;
          font-size: 16px;
          text-align: center;
        }
      }
      .footer-info {
        padding-top: 30px;
        font-size: 14px;
        p {
          padding: 10px 0;
        }
      }
    }
  }
</style>
