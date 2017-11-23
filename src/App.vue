<template>
  <div>
  <mt-header title="多个按钮">
  <router-link to="/" slot="left">
    <mt-button icon="back">返回</mt-button>
    <mt-button @click="">关闭</mt-button>
  </router-link>
  <mt-button icon="more" slot="right"></mt-button>
</mt-header>
<mt-swipe :auto="4000">
  <mt-swipe-item><img src="./assets/logo.png"></mt-swipe-item>
  <mt-swipe-item>2</mt-swipe-item>
  <mt-swipe-item>3</mt-swipe-item>
</mt-swipe>
    
    <router-view/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'app'
})
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
