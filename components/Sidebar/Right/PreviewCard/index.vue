<script setup>

const props = defineProps({
  title: {
    type: String,
    required: true
  }
})

const {twitterBorderColor, defaultTransition} = useTailwindConfig()

</script>

<template>

<div class="m-2 border rounded-xl bg-gray-50 dark:bg-dim-700"
     :class="twitterBorderColor">

  <h1 class="p-3 text-l font-extrabold text-gray-900 border-b dark:text-gray-200">
    {{ props.title }}
  </h1>

  <slot />

  <div class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300 rounded-xl"
       :class="defaultTransition">
    Show more
  </div>

</div>

</template>

<style scoped>

</style>