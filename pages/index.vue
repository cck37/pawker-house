<script lang="ts" setup>
const { t } = useLang()
const { theme } = useCurrentTheme()

// meta
definePageMeta({
  layout: 'page',
})

// vars
const titlesText = computed<string[]>(() => t('pages.index.title').split(','))
const sourcePath = computed<string>(() =>
  theme.value === 'dark' ? '/night_time.mp4' : '/sea_girt_drone_vid.mp4'
)
const firstCardText = computed<string>(() => t('pages.index.first_card'))
const firstCardImage = computed<string>(() => t('pages.index.first_image'))
</script>

<template>
  <div class="flex-1 relative pb-4">
    <div
      class="flex justify-center items-center h-screen w-screen overflow-hidden"
    >
      <div class="video-wrapper w-full h-full">
        <PageVideo
          :key="theme"
          :source="sourcePath"
          type="video/mp4"
          class="min-w-full min-h-full max-w-fit xl:min-w-0 xl:min-h-0"
        />
        <h1 class="text-center flex flex-col z-10 gap-11">
          <span
            v-for="(item, i) in titlesText"
            :key="i"
            class="text-shadow text-gray-200 text-5xl sm:text-7xl md:text-7xl lg:text-7xl xl:text-7xl 2xl:text-8xl dark:uppercase dark:dark-title block"
          >
            {{ item }}
          </span>
        </h1>
      </div>
    </div>
    <PageBody>
      <div>
        <div data-aos="fade-left">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
        <div data-aos="fade-right">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
        <div data-aos="fade-left">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
        <div data-aos="fade-right">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
        <div data-aos="fade-left">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
        <div data-aos="fade-right">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
        <div data-aos="fade-bottom">
          <card :text="firstCardText" :image="firstCardImage" />
        </div>
      </div>
    </PageBody>
  </div>
</template>

<style lang="scss">
$padding: 0.05em;
.text-shadow {
  text-shadow: 0 2px 4px theme('colors.slate.800');
}

video {
  object-fit: cover;
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
}

.video-wrapper {
  position: relative;
  width: 100%;
  height: 100%;
  overflow: hidden;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
