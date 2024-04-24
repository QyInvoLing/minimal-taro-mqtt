<template>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import './index.less'

const msg = ref('Hello world')
import mqtt from "mqtt"
onMounted(()=>{
  mqtt.connect("mqtt:localhost:25565")
})
</script>
