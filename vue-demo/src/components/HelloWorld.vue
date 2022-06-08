<!--
 * @Author: Tom
 * @LastEditors: Tom
 * @Date: 2022-06-08 12:01:05
 * @LastEditTime: 2022-06-08 12:11:09
 * @Email: Tom
 * @FilePath: \pp\src\components\HelloWorld.vue
 * @Environment: Win 10
 * @Description: 
-->
<template>
  <div>
    <canvas id="video-canvas" style="height: 540px; wight: 564px"></canvas>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      path: "ws://127.0.0.1:8082",
    }
  },
  mounted() {
    var canvas = document.getElementById("video-canvas")
    var player = new JSMpeg.Player(this.path, { canvas: canvas })
  },
}
</script>
