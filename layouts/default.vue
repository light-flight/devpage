<template lang='pug'>
  md-app
    md-app-content
      greeting-block
      nuxt
</template>

<script>
import GreetingBlock from '~/components/GreetingBlock.vue'
export default {
  components: {
    GreetingBlock
  },
  data: () => ({
    // showNavigation: false,
    // showSidepanel: false
  })
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
  width: 100%;
  overflow-x: hidden;
  font-family: 'Roboto Mono', monospace;
  padding: 0;
}
</style>
