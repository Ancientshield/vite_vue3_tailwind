<template>
  <div :class="['w-80 p-5', 'bg-gray-200', 'rounded-lg']">
    <div :class="['h-2 w-full', 'bg-green-800', 'rounded-full']">
      <div
        :class="['h-full w-1/3', 'bg-green-500', 'rounded-full']"
        :style="{
          width: percent + '%'
        }"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProgressBar',
  props: ['minVal', 'maxVal', 'currentVal'],
  data() {
    return {
      percent: 0
    }
  },
  mounted() {
    this.percent =
      this.currentVal <= this.minVal
        ? 0
        : ((this.currentVal - this.minVal) * 100) / (this.maxVal - this.minVal)
  },
  watch: {
    currentVal(newVal, oldVal) {
      this.percent =
        newVal <= this.minVal
          ? 0
          : ((newVal - this.minVal) * 100) / (this.maxVal - this.minVal)
    }
  }
}
</script>

<style></style>
