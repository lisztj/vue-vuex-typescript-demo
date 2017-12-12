<template>
<div class="tabbarnav">
<mt-tabbar v-model="selected" class="bottom-fixed">
  <mt-tab-item id="tab1">
    <img slot="icon" src="../assets/img.png">
    会员
  </mt-tab-item>
  <mt-tab-item id="tab2">
    <img slot="icon" src="../assets/img.png">
    tab2
  </mt-tab-item>
  <mt-tab-item id="tab3">
    <img slot="icon" src="../assets/img.png">
    tab3
  </mt-tab-item>
  <mt-tab-item id="tab4">
    <img slot="icon" src="../assets/img.png">
    我的
  </mt-tab-item>
</mt-tabbar>
</div>
</template>
<script lang="ts">
import Vue from 'vue'
import { mapGetters } from 'vuex'
import { CartProduct, CheckoutStatus } from '../store'
import Component from 'vue-class-component'
import { Getter, Action } from 'vuex-class'

@Component
export default class TabbarNav extends Vue {
  data() {  
    return {  
      selected: true  
    }
}
}

</script>
<style>
.bottom-fixed {
    right: 0;
    bottom: 0;
    left: 0;
    position: fixed;
    z-index: 1;
}
</style>
