<template>
  <div 
    :class="[
      [
        'w-20 h-20 bg-gray-500 rounded-md',
        'focus:ring-4 group-hover:text-gray-600',
        'font-bold text-3xl text-white',
        'flex justify-center items-center',
        'cursor-pointer outline-none'
      ],
      (color==='red') && 'bg-red-500 hover:bg-red-400 ring-red-300',
      (color==='blue') && 'bg-blue-500 hover:bg-blue-400 ring-blue-300',
      (color==='purple') && 'bg-purple-500 hover:bg-purple-400 ring-purple-300'
    ]"
    :tabindex="number"
  >
    {{ number }}
  </div>
</template>

<script>
export default {
  name: "Box",
  props: ["number", "color"]
}
</script>