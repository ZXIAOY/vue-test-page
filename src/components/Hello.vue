<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: '进入vue文件'
    }
  }
}
</script>

<style lang="scss" scoped>
  .hello {
    border: 1px solid red;
    h1 {
      color: yellow;
      &:hover {
        background-color: #777;
      }
    }
  }
</style>
