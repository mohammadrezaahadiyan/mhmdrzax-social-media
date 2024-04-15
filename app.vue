<template>
  <div :class="{'dark': darkMode}">

    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">

        <div class="grid grid-cols-12 mx-auto lg:mx-24 sm:px-6">

          <!-- Left bar-->
          <div class="hidden md:block md:col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <SidebarLeft />
            </div>
          </div>
          <!-- Main content-->

          <main class="grid col-span-12 md:col-span-8 xl:col-span-6">
            <RouterView />
          </main>

          <!-- Right bar-->

          <div class="hidden md:block md:col-span-3 xl:col-span-4 bg-amber-300">
            <div class="sticky top-0">
              <SidebarRight />
            </div>
          </div>

        </div>

      </div>
    </div>

  </div>

  <button @click="darkMode = !darkMode" class="border-red-900 border-2">
    change theme
  </button>
</template>

<script setup>
import 'public/assets/style/scss/main.css'
const darkMode = ref(false)
</script>