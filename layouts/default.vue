<template lang='pug'>
  md-app
    md-app-content
      nuxt
</template>

<script>
export default {
  components: {
  },
  data: function () {
    return {
      // showNavigation: false,
      // showSidepanel: false
    }
  }
}
</script>

<style lang='scss' scoped>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.md-app-content {
  font-family: 'Roboto Mono', monospace;
  border-left: none;
  border-right: none;
}
</style>
