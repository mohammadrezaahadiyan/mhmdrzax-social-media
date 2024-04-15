<script setup>
const { defaultTransition } = useTailwindConfig()

</script>

<template>

  <div class="">
    <NuxtLink to="#">
      <div class="flex flex-row rounded-full hover:bg-gray-100 p-3 items-center
                 dark:hover:bg-gray-800"
           :class="defaultTransition"
      >
        <div class="text-dim-900 mr-2.5 icon
             dark:text-gray-200">
          <slot name="icon"></slot>
        </div>

        <div class="text-xl text-dim-900 hidden md:block xs:w-full
                   dark:text-gray-200">
          <slot name="title"></slot>
        </div>
      </div>
    </NuxtLink>
    </div>

</template>

<style scoped>

</style>