<template>
  <div>Home</div>
  <div>用户名：{{ mainStore.name }}<br />长度：{{ mainStore.nameLength }}</div>
  <n-button @click="handleUpdateName">修改名称</n-button>
</template>
<script setup lang="ts">
import { useMainStore } from '@/store'
import { NButton } from 'naive-ui'

const mainStore = useMainStore()

function handleUpdateName() {
  //   mainStore.$patch({ name: '修改后的名称' })
  mainStore.insertPost('hi')
}
</script>
