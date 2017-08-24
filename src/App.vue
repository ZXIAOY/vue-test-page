<template>
  <div id="app">
    <zr-header></zr-header>
    <zr-download></zr-download>
  </div>
</template>

<script type='text/ecmascript-6'>
  import header from "./components/zr-header.vue";
  import download from "./components/zr-download.vue";
  export default {
    name: 'app',
    components: {
      'zr-header': header,
      'zr-download': download
    }
  }
</script>

<style type="text/scss" lang="scss">
  @import url("assets/cssReset.css");

</style>
