<script setup>
import { useUserStore } from '@/stores'
const userStore = useUserStore()
</script>

<template>
  <hr />
  <router-view></router-view>
  <hr />
  <hr />
  <hr />
  <div>我是APP</div>
  <text-demo></text-demo>
  <el-button type="primary">按钮一</el-button>
  <el-button>按钮二</el-button>

  <p>{{ userStore.token }}</p>
  <button @click="userStore.setToken('ILiveYou')">登录</button>
  <button @click="userStore.removeToken()">退出</button>
</template>

<style scoped></style>
