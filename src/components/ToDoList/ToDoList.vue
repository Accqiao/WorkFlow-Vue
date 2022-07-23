<template>
  <!-- <el-button :plain="true" @click="open">Show message</el-button>
  <el-button plain @click="open4"> Top Left </el-button> -->
  <el-row :gutter="20">
    <el-col :span="6">

    </el-col>
    <el-col :span="18">

      <el-timeline>
        <el-checkbox-group
          @change="handleCheckbox"
          v-model="checkList">
        <el-timeline-item
          v-for="(item, index) in doList"
          :key="index"
          :timestamp="item.updateTime"
        >
          <!-- <el-checkbox :label="item.id" /> -->
          <el-card>
            <span>{{item.content}}</span>
          </el-card>
        </el-timeline-item>
        </el-checkbox-group>
        <el-timeline-item timestamp="开始的开始~" placement="bottom">
        </el-timeline-item>
      </el-timeline>

    </el-col>
  </el-row>
</template>

<script lang='ts' setup>
import { ElMessage, ElNotification } from 'element-plus'
import { ref } from 'vue'
const doList = [
  {
    id:"1001",
    content:"apple",
    mark:"",
    finish: false,
    delete: false,
    updateTime: "2020-7-20",
    createTime: "2020-7-20",
  },
  {
    id:"1002",
    content:"banana",
    mark:"",
    finish: false,
    delete: false,
    updateTime: "2020-7-20",
    createTime: "2020-7-20",
  },
  {
    id:"1003",
    title:"",
    content:"cherry",
    mark:"",
    finish: true,
    delete: false,
    updateTime: "2020-7-20",
    createTime: "2020-7-20",
  },
  {
    id:"1004",
    content:"lemon",
    mark:"",
    finish: true,
    delete: false,
    updateTime: "2020-7-20",
    createTime: "2020-7-20",
  },
  {
    id:"1005",
    content:"mango",
    mark:"",
    finish: false,
    delete: false,
    updateTime: "2020-7-20",
    createTime: "2020-7-20",
  },
  {
    id:"1006",
    content:"orange",
    mark:"",
    finish: false,
    delete: false,
    updateTime: "2020-7-20",
    createTime: "2020-7-20",
  },]

const checkList = ref(['Option A'])

const handleCheckbox = (value: string[])=>{
  console.log(value)
}

const open = () => {
  ElMessage({
    message: 'this is a message Test 2.0 !',
    grouping: true,
    type: 'success',
    center: true,
    showClose: true,
  })
}
const open4 = () => {
  ElNotification({
    title: 'Custom Position',
    message: "I'm at the top left corner",
    type: 'info',
    position: 'top-right',
  })
}
</script>

<style scoped>
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.box-card {
  width: 480px;
}
</style>
