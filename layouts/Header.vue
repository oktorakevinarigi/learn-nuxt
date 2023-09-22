<template>
  <div class="border-b border-b-[#EAEAEA]">
    <SimpleBlock class="flex justify-between h-[84px] items-center">
      <div class="flex gap-4 items-center">
        <img src="/icon/logo.svg" alt="logo" />
        <p>alem<span class="font-extrabold">help</span></p>
      </div>
      <div class="flex gap-4">
        <button class="btn capitalize bg-[#F48023] text-white px-5 py-3 rounded-[5px]">
          <img src="/icon/user.svg" alt="icon user" /> Register
        </button>
        <button class="px-5 py-3 btn capitalize text-[#1682FD] rounded-[5px]">Login</button>
      </div>
    </SimpleBlock>
  </div>
</template>

<script lang="ts" setup>
import SimpleBlock from "./SimpleBlock.vue";
</script>

<style></style>
