<template>
  <div>
      <mt-header title="多个按钮">
  <router-link to="/" slot="left">
    <mt-button icon="back">返回</mt-button>
  </router-link>
  <mt-button icon="more" slot="right" :actions="actions" v-model="sheetVisible"></mt-button>
</mt-header>
        <mt-cell title="商品" is-link>
  <span></span>
</mt-cell>
  <mt-cell title="标题文字" is-link>
  <span style="color: green">这里是元素</span>
</mt-cell>
<mt-cell title="标题文字">
  <span>icon 是图片</span>
  <img slot="icon" src="../assets/img.png" width="24" height="24">
</mt-cell>
<mt-cell title="sddsd">
<div class="mint-cell-value"><button class="mint-button mint-button--primary mint-button--small"><span class="mint-button-icon"><i class="mintui mintui-back"></i></span> <label class="mint-button-text">按钮</label></button></div>
</mt-cell>
    <product-list></product-list>
    <hr>
    <cart></cart>

    <mt-actionsheet
  :actions="actions"
  v-model="sheetVisible">
</mt-actionsheet>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ProductList from './ProductList.vue'
import Cart from './Cart.vue'
export default Vue.extend({
  components: { ProductList, Cart }
})

</script>
