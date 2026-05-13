<template>
  <button
    type="button"
    class="robo-banner group absolute top-32 sm:top-48 lg:top-44 xl:top-50 right-10 sm:right-auto left-auto sm:left-5 xl:left-8 w-[316px] h-[87px] origin-top-right sm:origin-top-left scale-75 lg:scale-100 xl:scale-125 rotate-[-10deg] p-0 border-0 bg-transparent cursor-pointer"
    aria-label="Open info dialog"
    @click="$emit('click', $event)"
  >
    <img
      src="/images/banners/robo-calm.svg"
      alt=""
      class="absolute inset-0 w-full h-full select-none pointer-events-none group-hover:opacity-0"
      draggable="false"
    />
    <img
      src="/images/banners/robo-angry.svg"
      alt=""
      class="absolute inset-0 w-full h-full select-none pointer-events-none opacity-0 group-hover:opacity-100"
      draggable="false"
    />
  </button>
</template>

<script setup lang="ts">
defineEmits<{
  (e: 'click', event: MouseEvent): void
}>()
</script>

<style lang="postcss" scoped>
.robo-banner {
  z-index: 40;
}
</style>
