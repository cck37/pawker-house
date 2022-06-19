<script lang="ts" setup>
// micro compiler
const props = defineProps({
  text: {
    type: String,
    default: '',
  },
  image: {
    type: String,
    default: '',
  },
  link: {
    type: String,
    default: '',
  },
})
</script>

<template>
  <!-- Container -->
  <div class="container mt-32 mx-auto p-4 md:p-0">
    <div
      class="flex p-2 lg:bg-cover sm:bg-auto lg:bg-right sm:bg-top bg-no-repeat border-2 border-black dark:border-white"
      :style="`background-image: url(/${props.image}) `"
    >
      <div
        class="w-full p-8 mt-40 text-center bg-white dark:bg-slate-800 sm:mt-0 sm:w-1/2 sm:py-16"
      >
        <h5 class="max-w-xs mx-auto text-lg font-bold sm:text-base break-words">
          {{ props.text }}
        </h5>

        <a :href="props.link" target="_blank" class="mt-4 text-xs font-medium"
          >Learn More</a
        >
      </div>
    </div>
  </div>
  <!-- ./Container -->
</template>
