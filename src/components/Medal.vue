<template>
  <div>
    <div class="medal m-medal__fans-medal-item" :style="'border-color:' + colorBorderHex">
      <div class="m-medal__fans-medal-label"
           :style="'background-image: linear-gradient(45deg,' + colorStartHex + ',' + colorEndHex +');'">
        <span class="m-medal__fans-medal-content">{{ name }}</span>
      </div>
      <div class="m-medal__fans-medal-level" :style="'color:' + colorBorderHex">
        {{ level }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    colorStart: Number,
    colorEnd: Number,
    colorBorder: Number,
    level: Number,
    name: String
  },
  computed: {
    colorStartHex: function () {
      return '#' + this.colorStart.toString(16)
    },
    colorEndHex: function () {
      return '#' + this.colorEnd.toString(16)
    },
    colorBorderHex: function () {
      return '#' + this.colorBorder.toString(16)
    }
  }
}
</script>

<style scoped>

</style>
