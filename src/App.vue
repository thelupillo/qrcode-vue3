<template>
  <QrCodeScanner />
</template>

<script>
import QrCodeScanner from './components/QrCodeScanner.vue'

export default {
  name: 'App',
  components: {
    QrCodeScanner
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
