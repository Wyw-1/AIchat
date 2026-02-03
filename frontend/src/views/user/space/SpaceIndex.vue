<script setup>
import {useRoute, useRouter} from "vue-router";

const route=useRoute()//route调用当前url参数


</script>

<template>
个人空间:{{route.params.user_id}}
</template>

<style scoped>

</style>