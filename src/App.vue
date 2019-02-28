<template>
  <div id="app2">
    <img src="./assets/logo.png">
    <div>
      <el-button @click="startHacking">StartMe2</el-button>
    </div>

    <el-button @click="show = !show" style="margin-top:10px;">Click Me</el-button>

    <div style="display: flex; margin-top: 20px; height: 100px;">
      <transition name="el-fade-in-linear">
        <div v-show="show" class="transition-box">.el-fade-in-linear</div>
      </transition>
      <transition name="el-fade-in">
        <div v-show="show" class="transition-box">.el-fade-in</div>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
      show: true
  }),
  methods: {
    startHacking () {
      this.$notify({
        title: '小红，It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    }
  }
}
</script>

<style>
#app2 {
  font-family: Helvetica, sans-serif;
  text-align: center;
}

.transition-box {
  margin-bottom: 10px;
  width: 200px;
  height: 100px;
  border-radius: 4px;
  background-color: #409EFF;
  text-align: center;
  color: #fff;
  padding: 40px 20px;
  box-sizing: border-box;
  margin-right: 20px;
}
</style>
