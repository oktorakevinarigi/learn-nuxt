<template>
  <div class="w-[310px] bg-white flex flex-col h-[calc(100vh-84px)]">
    <div class="flex-1">
      <div class="px-[50px] flex items-center pb-3 pt-8 gap-3 mb-8">
        <img src="/icon/search.svg" alt="icon search" />
        <p class="font-medium text-sm py-3 h-10">Search</p>
      </div>
      <p class="text-[#808080] font-medium text-xs pb-3 px-[50px]">MENU</p>
      <ul class="flex flex-col gap-3">
        <li class="font-medium text-sm py-3 bg-[#FCF4EC] px-[50px] flex gap-3">
          <img src="/icon/list.svg" alt="icon list" />
          <p>Questions</p>
        </li>
        <li class="font-medium text-sm py-3 px-[50px] flex gap-3">
          <img src="/icon/tag.svg" alt="icon tag" />
          <p>Tags</p>
        </li>
        <li class="font-medium text-sm py-3 px-[50px] flex gap-3">
          <img src="/icon/award.svg" alt="icon award" />
          <p>Ranking</p>
        </li>
      </ul>
    </div>

    <div class="flex gap-5 justify-center mb-10">
      <img src="/icon/github.svg" alt="icon github" />
      <img src="/icon/instagram.svg" alt="icon instagram" />
      <img src="/icon/facebook.svg" alt="icon facebook" />
    </div>
  </div>
</template>
