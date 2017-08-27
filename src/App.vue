<template>
  <div id="app">
    <zr-header></zr-header>
    <zr-download></zr-download>
    <zr-content></zr-content>
    <zr-footer></zr-footer>
  </div>
</template>

<script type='text/ecmascript-6'>
  import header from "./components/zr-header.vue";
  import download from "./components/zr-download.vue";
  import content from "./components/zr-content.vue";
  import footer from "./components/zr-footer.vue"

  export default {
    name: 'app',
    components: {
      'zr-header': header,
      'zr-download': download,
      'zr-content': content,
      'zr-footer': footer
    }
  }
</script>

<style type="text/scss" lang="scss">
  @import url("assets/cssReset.css");

</style>
