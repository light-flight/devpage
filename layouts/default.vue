<template lang='pug'>
  md-app
    md-app-drawer(md-permanent='full')
      .background
      drawer
    md-app-content
      nuxt
</template>

<script>
import Drawer from '~/components/Drawer.vue'
export default {
  components: {
    Drawer
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
  margin: 0;
}

.md-drawer {
  width: 280px;
  max-width: calc(100vw - 125px);
  min-height: 100vh;
}

.background {
    position: fixed;
    width: 100%;
    height: 100%;
    background-image: url(~/assets/images/3.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    filter: blur(15px) brightness(0.82);
    transform: scale(1.2);
  }

.md-app-content {
  font-family: 'Roboto Mono', monospace;
}
</style>
