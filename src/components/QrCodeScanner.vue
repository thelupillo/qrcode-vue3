<template>
  <div class="qrstream">
      <qr-stream @decode="onDecode"></qr-stream>
      <span>{{ state.qrDecoded }}</span>
  </div>
</template>

<script>
import { reactive } from 'vue';
import { QrStream } from 'vue3-qr-reader';

export default {
    name: "QrCodeScanner",
    setup() {
        const state = reactive({
            qrDecoded: {
                type: String
            }
        });

        function onDecode(decodedString) {
            state.qrDecoded = decodedString;
        }

        return {
            state,
            onDecode
        }
    },
    components: {
        QrStream
    }
}
</script>

<style scoped>
.qrstream {
    height: 90vh;
    width: 90vw;
    position: absolute;
    top: 50vh;
    left: 50vw;
    transform: translate(-50%, -50%);
}
</style>