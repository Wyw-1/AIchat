<script setup>

import MenuIcon from "@/components/navbar/icons/MenuIcon.vue";
import HomepageIcon from "@/components/navbar/icons/HomepageIcon.vue";
import FriendIcon from "@/components/navbar/icons/FriendIcon.vue";
import CreateIcon from "@/components/navbar/icons/CreateIcon.vue";
import SearchIcon from "@/components/navbar/icons/SearchIcon.vue";
</script>

<template>
  <div class="drawer lg:drawer-open">
    <input id="my-drawer-4" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content">
      <nav class="navbar w-full bg-base-100 shadow-xl">
        <div class="navbar-start">
          <label for="my-drawer-4" aria-label="open sidebar" class="btn btn-square btn-ghost">
            <MenuIcon/>
          </label>
          <div class="px-4 font-bold text-xl" >AIFriends</div>
        </div>
        <div class="navbar-center absolute left-1/2 -translate-x-1/2">
          <div class="join">
            <input class="input join-item rounded-l-full w-96" placeholder="搜索你感兴趣的内容" />
            <button class="btn join-item rounded-r-full gap-0">
              <SearchIcon/>
              搜索
            </button>

          </div>
        </div>
        <div class="navbar-end">
          <RouterLink :to="{name:'user-account-login-index'}" active-class="btn-active" class="btn btn-neutral btn-outline">
            登录
          </RouterLink>
        </div>

      </nav>
      <slot></slot>
    </div>

    <div class="drawer-side is-drawer-close:overflow-visible">
      <label for="my-drawer-4" aria-label="close sidebar" class="drawer-overlay"></label>
      <div class="flex min-h-full flex-col items-start bg-base-200 is-drawer-close:w-15 is-drawer-open:w-64">
        <ul class="menu w-full grow">
          <li>
            <RouterLink :to="{name:'homepage-index'}" active-class="menu-focus" class="is-drawer-close:tooltip is-drawer-close:tooltip-right" data-tip="首页">
              <Homepage-icon/>
              <span class="is-drawer-close:hidden test-base ml-2 py-1 whilespace-nowrap">首页</span>
            </RouterLink>
          </li>

          <li>
            <RouterLink :to="{name:'friend-index'}"  active-class="menu-focus" class=" is-drawer-close:tooltip is-drawer-close:tooltip-right" data-tip="好友">
              <FriendIcon/>
              <span class="is-drawer-close:hidden test-base ml-2 py-1 whilespace-nowrap">好友</span>
            </RouterLink>
          </li>

          <li>
<!--            routerlink通过点击创作按钮，跳转到创作页面。点击创作->修改url->到创作页面-->
            <RouterLink :to="{name:'create-index'}" active-class="menu-focus" class="is-drawer-close:tooltip is-drawer-close:tooltip-right" data-tip="创作">
              <CreateIcon/>
              <span class="is-drawer-close:hidden test-base ml-2 py-1 whilespace-nowrap">创作</span>
            </RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>