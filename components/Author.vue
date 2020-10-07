<template>
  <div class="flex align-center items-center">
    <img class="rounded-full w-16 h-16 object-cover" :src="author.image" />
    <div class="px-2 text-gray-700">
      <p class="font-bold">{{ author.name }}</p>
      <p>{{ author.bio }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>