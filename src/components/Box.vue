<template>
  <div
    :class="[
      [
        'h-20 w-20 rounded-md bg-gray-500',
        'focus:ring-4 group-hover:text-gray-600',
        'text-3xl font-bold text-white',
        'flex items-center justify-center',
        'cursor-pointer outline-none'
      ],
      color === 'red' && 'bg-red-500 ring-red-300 hover:bg-red-400',
      color === 'blue' && 'bg-blue-500 ring-blue-300 hover:bg-blue-400',
      color === 'purple' && 'bg-purple-500 ring-purple-300 hover:bg-purple-400'
    ]"
    :tabindex="number"
  >
    {{ number }}
  </div>
</template>

<script>
export default {
  name: 'Box',
  props: ['number', 'color']
}
</script>
