<template>
  <div class="flex justify-evenly p-10 focus-within:bg-green-100 group">
    <box v-for="item in Boxes" v-bind="item" :key="item.number" />
  </div>
  <div :class="['w-screen h-screen',
    'flex flex-col',
    'justify-center items-center',
    'gap-5',
  ]">
    <input type="range" v-model="val" :min="min" :max="max" />
    <ProgressBar :currentVal="val" :minVal="min" :maxVal="max" />
  </div>
</template>

<script>
import Box from './components/Box.vue'
import ProgressBar from './components/ProgressBar.vue'

export default {
  data() {
    return {
      min: 0,
      max: 200,
      val: 100,
      // 定義三個 box 的內容
      Boxes: [
        {number: 5, color: 'blue'},
        {number: 2, color: 'purple'},
        {number: 0, color: 'red'},
      ]
    }
  },
  components: {
    ProgressBar,
    Box
  }
}
</script>