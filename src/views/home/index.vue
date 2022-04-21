<script setup lang="ts">
import { useRouter } from 'vue-router'
import { h, getCurrentInstance } from 'vue'
const router = useRouter()
const { proxy } :any = getCurrentInstance()
proxy.$message({
  message: h('p', null, [
    h('span', null, 'Message can be '),
    h('i', { style: 'color: teal' }, 'VNode'),
  ]),
})
</script>

<template>
  首页
  <el-button>defult</el-button>
  <button @click="() => router.push( { path : '/mine', query: { id : 1}})">跳转到个人中心</button>
</template>

<style>
</style>
