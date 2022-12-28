<template>
  <div class="flex justify-evenly p-10 focus-within:bg-green-100 group">
    <box v-for="item in Boxes" v-bind="item" :key="item.number" />
  </div>
</template>

<script>
import Box from './components/Box.vue'

export default {
  data() {
    return {
      // 定義三個 box 的內容
      Boxes: [
        {number: 5, color: 'blue'},
        {number: 2, color: 'purple'},
        {number: 0, color: 'red'},
      ]
    }
  },
  components: {
    Box
  }
}
</script>