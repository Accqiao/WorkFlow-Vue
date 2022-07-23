<template>
  <el-page-header content="detail" @back="goBack" />
</template>

<script lang='ts' setup>
//import {useRouter,useRoute} from 'vue-router';
const goBack = () => {
  console.log('go back')
}
</script>

<style scoped>

</style>
