<script setup>
import {useRoute, useRouter} from "vue-router";

const route=useRoute()//route调用当前url参数
const router=useRouter()//router用于页面前进或后退...
router.push({
  name:'homepage-index'
})

</script>

<template>
个人空间:{{route.params.user_id}}
</template>

<style scoped>

</style>