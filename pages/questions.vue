<template>
  <NuxtLayout name="content">
    <div class="flex gap-5 mb-9">
      <FilterChip />
    </div>

    <div class="flex flex-col gap-6">
      <CardContent v-for="item in Array.from(Array(3).keys())" :key="item" />
    </div>
  </NuxtLayout>
</template>

<script lang="ts" setup></script>

<style></style>
