<template>
  <el-select v-model="value" item placeholder="Select" @change="handleChange">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value"
    />
  </el-select>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const value = ref('')

const options = [
  {
    value: 1,
    label: '张三',
  },
  {
    value: 2,
    label: '李四',
  },
  {
    value: 3,
    label: '王五',
  },
]
//select加入item属性 第二个参数可以返回整个对象 方便给后端赋值
function handleChange(value, itemObjs) {
  console.log(value, '-------value')
  console.log(itemObjs.label, '-------itemObjs.label')
}
</script>
