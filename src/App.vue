<template>
  <div id="app">
    <zr-header></zr-header>
    <div class="content">
    </div>
  </div>
</template>

<script type='text/ecmascript-6'>
  import header from "./components/zr-header.vue"
  export default {
    name: 'app',
    components: {
      'zr-header': header,
    }
  }
</script>

<style type="text/scss" lang="scss">
  @import url("assets/cssReset.css");
  .content {
    height: 1000px;
    margin: 80px;
  }
</style>
