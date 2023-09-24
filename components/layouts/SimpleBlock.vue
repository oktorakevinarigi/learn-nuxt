<template>
  <div :class="cn('me-auto ms-auto w-full max-w-[1200px] px-5 xl:px-0', props.class)">
    <slot />
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  class: { type: String, default: "" },
});
</script>

<style></style>
