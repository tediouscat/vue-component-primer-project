<script setup>
import Header from "./components/header.vue";
import Footer from "./components/footer.vue";
import {reactive} from "vue";

const propsWeb=reactive({
  user:10,
  url:"www.baidu.com"
})

const userAdd=()=>{
  propsWeb.user++;
}
</script>

<template>

  <Header propsName="tediouscat" propsUrl="www.baidu.com"/>
  content
  <Footer v-bind="propsWeb"/>
  <button @click="userAdd">点击按钮</button>

</template>

<style scoped>

</style>
