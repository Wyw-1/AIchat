<script setup>
import {useUserStore} from "@/stores/user.js";

const user=useUserStore()
</script>

<template>
  <div class="dropdown dropdown-end">
    <div tabindex="0" role="button" class="avatar btn btn-circle w-8 h-8 mr-6">
      <div class="w-8 rounded-full">
        <img :src="user.photo" alt="">
      </div>
    </div>
    <ul tabindex="-1" class="dropdown-content menu bg-base-100 rounded-box z-1 w-52 p-2 shadow-sm">
      <li>
        <RouterLink :to="{name:'user-space-index',params:{user_id:user.id}}">
          <div class="avatar">
            <div class="w-10 rounded-full">
              <img :src="user.photo" alt="">
            </div>
          </div>
          <span class="text-base line-clamp-1">{{user.username}}</span>
        </RouterLink>
      </li>
    </ul>
  </div>
</template>

<style scoped>

</style>