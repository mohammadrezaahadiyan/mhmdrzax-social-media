<script setup lang="ts">

const {defaultTransition} = useTailwindConfig()

const whatsHappenings = ref([
  {
    title:"#spaceX",
    count: "18.8k Tweets"
  },{
    title:"#CodingIsFun",
    count: "18.8k Tweets"
  },{
    title:"#ArtForAll",
    count: "18.8k Tweets"
  }
])

const whoToFollows = ref([
  {
    name: "Mohammadreza",
    username: "mhmdrzaxhd",
    imageName: "/public/assets/images/photo-1505904267569-f02eaeb45a4c.avif"
  },{
    name: "Alireza",
    username: "alirezax",
    imageName: "/public/assets/images/photo-1505904267569-f02eaeb45a4c.avif"
  },{
    name: "Arshiya",
    username: "arshix",
    imageName: "/public/assets/images/photo-1505904267569-f02eaeb45a4c.avif"
  },

])

</script>

<template>
  <div class="flex flex-col">

    <div>
      <SidebarRightPreviewCard title="What's happening">

        <SidebarRightPreviewCardItem v-for="(item, index) in whatsHappenings" :key="index">

          <h2 class="text-l my-1">
            {{ item.title }}
          </h2>

          <p class="text-xs mb-2">
            {{ item.count }}
          </p>

        <hr />
        </SidebarRightPreviewCardItem>

      </SidebarRightPreviewCard>
    </div>
    <div>
      <SidebarRightPreviewCard title="Who to follow">

        <SidebarRightPreviewCardItem v-for="(item, index) in whoToFollows" :key="index">

          <div class="flex flex-row items-center justify-between">

            <div class="flex items-center">

              <div class="w-10 h-10 rounded-full">
                <img src="/public/assets/images/photo-1505904267569-f02eaeb45a4c.avif" :alt="item.username" class="object-cover object-center w-10 h-10 rounded-full">
              </div>

              <div class="ml-2 leading-1 mb-2">

                <h6 class="text-lg">
                  {{ item.username }}
                </h6>
                <span class="text-xs">
                {{ item.name }}
              </span>

              </div>

            </div>

            <div class="bg-black hover:bg-black/80 dark:bg-white dark:hover:bg-white/80 rounded-3xl px-4 py-1"
                 :class="defaultTransition">
              <button>
                <span class="text-white font-bold text-xs dark:text-black">
                  Follow
                </span>
              </button>
            </div>

          </div>
          <hr />
        </SidebarRightPreviewCardItem>

      </SidebarRightPreviewCard>
    </div>

  </div>
</template>

<style scoped>

</style>