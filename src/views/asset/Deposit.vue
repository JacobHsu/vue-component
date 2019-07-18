<template>
  <div class="asset-deposit">
      <qrcode-vue :value="assetAddress"></qrcode-vue>
      {{assetAddress}}
  </div>
</template>

<script>
import QrcodeVue from 'qrcode.vue';

export default {
  name: 'AssetDeposit',
  components: {
    QrcodeVue
  },
  computed: {
    assetAddress() {
        return this.$store.state.asset.address || {}
    },
  }
}
</script>