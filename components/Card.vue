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
})
</script>

<template>
  <!-- Container -->
  <div class="container mt-32 mx-auto p-4 md:p-0">
    <!-- Card wrapper -->
    <div class="shadow-lg flex flex-wrap w-full lg:w-4/5 mx-auto">
      <!-- Card image -->
      <div
        class="bg-cover bg-no-repeat bg-bottom rounded border-2 dark:border-gray-700 w-full md:w-1/3 lg:h-96 md:h-auto relative"
        :style="`background-image: url(../public/${props.image})`"
      ></div>
      <!-- ./Card image -->

      <!-- Card body -->
      <div class="bg-white dark:bg-gray-900 w-full md:w-2/3">
        <!-- Card body - outer wrapper -->
        <div class="h-full mx-auto px-6 md:px-0 md:pt-6 md:-ml-6 relative">
          <!-- Card body - inner wrapper -->
          <div
            class="bg-white rounded border-2 dark:border-gray-700 dark:bg-gray-900 lg:h-full p-6 -mt-6 md:mt-0 relative mb-4 md:mb-0 flex flex-wrap md:flex-wrap items-center"
          >
            <!-- Card description -->
            <div class="w-full lg:w-3/5 lg:px-3">
              <p class="text-md mt-4 lg:mt-0 text-justify md:text-left text-sm">
                {{ props.text }}
              </p>
            </div>
            <!-- ./Card description -->

            <!-- Call to action button -->
            <div
              class="w-full lg:w-1/5 mt-6 lg:mt-0 lg:px-4 text-center md:text-left"
            >
              <button
                class="bg-white dark:bg-gray-900 hover:dark:bg-gray-700 hover:bg-light-300 border border-solid border-gray w-1/3 lg:w-full py-2"
              >
                Visit now
              </button>
            </div>
            <!-- ./Call to action button -->
          </div>
          <!-- ./Card body - inner wrapper -->
        </div>
        <!-- ./Card body - outer wrapper -->
      </div>
      <!-- ./Card body -->
    </div>
    <!-- ./Card wrapper -->
  </div>
  <!-- ./Container -->
</template>
