<script setup>
import { reactive,ref } from 'vue'
//导入子组件
import Header from "./component/header.vue"

//响应式数据
const web = reactive({
  name: "邓瑞编程",
  url: 'dengruicode.com'
})

const user = ref(0)

//子传父
const emitsWeb = (data) => {
  console.log("emitsWeb:",data)
  web.url = data.url
}

const emitsUser = (data) => {
  console.log("emitsUser:",data)
  user.value += data
}
</script>

<template>
  <!-- 子传父 -->
  <Header @web="emitsWeb" @user="emitsUser" />

  {{ web.url }} - {{ user }}
</template>

<style scoped>

</style>
