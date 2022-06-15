<script lang="ts" setup>
definePageMeta({
  layout: 'page',
})
</script>

<template>
  <PageWrapper class="flex flex-col justify-center items-center">
    <PageHeader>
      <PageTitle :text="$t('pages.about.title')" class="capitalize" />
    </PageHeader>
    <PageBody>
      <div class="flex flex-col items-center gap-y-4">
        <div class="text-2xl font-bold w-80 text-center pb-2">
          {{ $t('pages.about.description') }}
        </div>
        <img
          src="https://avatars.githubusercontent.com/u/20689555?v=4"
          class="inline-block rounded-full"
          alt="cck37"
          width="150"
          height="150"
        />
        <Button
          size="xs"
          text="Chris Kennedy (@cck37)"
          class="font-extrabold mt-4"
          href="https://github.com/cck37"
        />
      </div>
    </PageBody>
  </PageWrapper>
</template>
