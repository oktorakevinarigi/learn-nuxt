<template>
  <div
    :class="
      cn(
        'px-3 rounded-full py-1 flex gap-1 items-center cursor-pointer',
        selected === 'new' ? 'bg-[#1682FD] text-white' : 'bg-[#EAEAEA] text-[#808080]'
      )
    "
    @click="onSelected('new')"
  >
    <img src="/icon/clock.svg" alt="icon clock" />
    <p>New</p>
  </div>
  <div
    :class="
      cn(
        'px-3 rounded-full py-1 flex gap-1 items-center cursor-pointer',
        selected === 'top' ? 'bg-[#1682FD] text-white' : 'bg-[#EAEAEA] text-[#808080]'
      )
    "
    @click="onSelected('top')"
  >
    <img src="/icon/arrow-up-right.svg" alt="icon arrow-up-right" />
    <p>Top</p>
  </div>
  <div
    :class="
      cn(
        'px-3 rounded-full py-1 flex gap-1 items-center cursor-pointer',
        selected === 'hot' ? 'bg-[#1682FD] text-white' : 'bg-[#EAEAEA] text-[#808080]'
      )
    "
    @click="onSelected('hot')"
  >
    <img src="/icon/whh_hot.svg" alt="icon whh_hot" />
    <p>Hot</p>
  </div>
  <div
    :class="
      cn(
        'px-3 rounded-full py-1 flex gap-1 items-center cursor-pointer',
        selected === 'closed' ? 'bg-[#1682FD] text-white' : 'bg-[#EAEAEA] text-[#808080]'
      )
    "
    @click="onSelected('closed')"
  >
    <img src="/icon/check-circle.svg" alt="icon check-circle" />
    <p>Closed</p>
  </div>
</template>

<script lang="ts" setup>
const selected = ref("");

function onSelected(params: "top") {
  selected.value = params;
}
</script>

<style></style>
