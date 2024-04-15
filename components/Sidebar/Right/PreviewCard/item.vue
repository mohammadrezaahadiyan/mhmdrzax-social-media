<script setup lang="ts">

const {twitterBorderColor, defaultTransition} = useTailwindConfig()
const classWrapper = computed(() => `${twitterBorderColor} ${defaultTransition}`)

</script>

<template>

  <div class="p-3 hover:bg-gray-100 cursor-pointer dark:hover:bg-dim-300 text-gray-900 dark:text-gray-300"
       :class="classWrapper">

    <slot />

  </div>

</template>

<style scoped>

</style>