<script setup>
import {HomeIcon, MagnifyingGlassIcon, BellIcon, EnvelopeIcon, ClipboardDocumentListIcon, BookmarkIcon, UserIcon, EllipsisHorizontalCircleIcon} from "@heroicons/vue/24/outline/index.js";

const { defaultTransition } = useTailwindConfig()

const leftBarMaterials = [
  {title: "Home", element: HomeIcon},
  {title: "Search", element: MagnifyingGlassIcon},
  {title: "Notifications", element: BellIcon},
  {title: "Messages", element: EnvelopeIcon},
  {title: "List", element: ClipboardDocumentListIcon},
  {title: "Bookmarks", element: BookmarkIcon},
  {title: "Profile", element: UserIcon},
  {title:"More", element: EllipsisHorizontalCircleIcon}
]

</script>

<template>
  <div class="h-screen flex flex-col">

    <div class="p-2 my-2 hover:bg-blue-50 rounded-full w-12
         dark:hover:bg-white/20"
         :class={defaultTransition}
    >
    <NuxtLink to="/">
    <div class="w-8 h-8">
      <LogoTwitter />
    </div>
    </NuxtLink>
    </div>

    <SidebarLeftTab v-for="(material, index) in leftBarMaterials" :key="index">

       <template #icon>
        <component :is="material.element" />
       </template>

      <template #title>
        {{ material.title }}
      </template>
    </SidebarLeftTab>


  </div>
</template>

<style scoped>

</style>