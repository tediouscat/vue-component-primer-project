<script setup>
  const props=defineProps({
    user:Number,
    url:{
      type:String,
      required:false,
      default:'https://www.baidu.com'
    }
  })
  console.log(props)
</script>

<template>
  <hr>
  footer
  {{props.user}}
</template>

<style scoped>

</style>
