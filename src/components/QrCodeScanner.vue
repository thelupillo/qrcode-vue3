<template>
  <div>
      <qr-stream class="qrstream"></qr-stream>
  </div>
</template>

<script>
import { QrStream } from 'vue3-qr-reader';

export default {
    name: "QrCodeScanner",
    components: {
        QrStream
    }
}
</script>

<style scoped>
.qrstream {
    height: 100vh;
    width: 100vw;
    margin: 0;
    padding: 0;
}
</style>