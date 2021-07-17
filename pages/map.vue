<template>
  <div id="map">
    <client-only>
      <l-map minZoom="6" :zoom="zoom" :center="center">
        <l-tile-layer
          layerType="base"
          :attribution="attribution"
          :url="url"
        ></l-tile-layer>
      </l-map>
    </client-only>
  </div>
</template>

<script>
export default {
  data() {
    return {
      center: [38.856355, 141.615593],
      zoom: 13,
      url: 'https://cyberjapandata.gsi.go.jp/xyz/std/{z}/{x}/{y}.png',
      attribution:
        '<a href="https://maps.gsi.go.jp/development/ichiran.html" target="_blank">地理院タイル</a>',
    }
  },
}
</script>

<style scoped>
#map {
  position: absolute;
  top: 0px;
  left: 0px;
  right: 0px;
  bottom: 0px;
}
</style>
