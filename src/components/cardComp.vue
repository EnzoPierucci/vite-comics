<script>
export default {
  name: 'CardComp',
  props: {
    comic: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
<div class="max-w-sm rounded overflow-hidden shadow-lg">
    <img :src="comic.thumb" :alt="comic.series" class="w-full">
    <div class="p-4">
      <h3 class="font-bold">{{ comic.series }}</h3>
      <p class="text-gray-600">{{ comic.type }}</p>
      <p class="text-gray-800">{{ comic.price }}</p>
    </div>
  </div>


</template>

<style scoped>

</style>