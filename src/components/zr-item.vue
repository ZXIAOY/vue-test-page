<template>
  <div class="zr-item">
    <a href="#" class="item-link">
      <img :src="itemSrc" :alt="itemTitle" class="item-pic">
      <span class="item-title">{{itemTitle}}</span>
    </a>
  </div>
</template>

<script type='text/ecmascript-6'>
  export default {
    data: function () {
      return {

      }
    },
    props: ["itemTitle", "itemSrc"]
  }
</script>

<style type="text/scss" lang="scss">
  .zr-item:nth-child(3n+1) {
    margin-left: 0;
  }
  .zr-item {
    margin-left: 25px;
    margin-bottom: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 2px;
    .item-link {
      display: block;
      position: relative;
      text-decoration: none;
      .item-pic {
        display: block;
        margin-bottom: 10px;
        /*width: 280px;*/
        max-width: 100%;
        height: 260px;
      }
      .item-title {
        display: block;
        font-size: 16px;
        line-height: 30px;
        color: #000;
        background-color: #fff;
      }
    }
  }

</style>
