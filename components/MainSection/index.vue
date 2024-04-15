<script setup>

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  loading: {
    type: Boolean,
    required: true
  }
})

</script>

<template>

  <div>

    <div class="sticky top-0 bg-gray-100 px-4 py-3 font-bold mb-7
                dark:bg-dim-700 text-gray-200">
      <h2>{{ props.title }}</h2>
    </div>

    <div v-if="props.loading">
      <div class="flex items-center justify-center">
        <UISpinner/>
      </div>
    </div>

    <div v-else>
      <slot />
    </div>

  </div>

</template>

<style scoped>

</style>