<template>
  <div>
    <TheHeader />
    <div class="flex">
      <TheSidebar />
      <div class="px-[50px] py-5 w-full">
        <slot />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>
