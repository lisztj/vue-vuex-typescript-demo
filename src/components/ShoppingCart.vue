<template>
  <div>
      <mt-header title="多个按钮">
  <router-link to="/" slot="left">
    <mt-button icon="back">返回</mt-button>
  </router-link>
  <mt-button icon="more" slot="right" @click="actionSheet"></mt-button>
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
  :actions="data"
  v-model="sheetVisible">
</mt-actionsheet>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ProductList from './ProductList.vue'
import Cart from './Cart.vue'
export default Vue.extend({
  components: { ProductList, Cart },
  data () {
    return {
      // action sheet 选项内容  
      data: [{  
        name: '拍照',  
        method : this.getCamera// 调用methods中的函数  
      }, {  
        name: '从相册中选择',   
        method : this.getLibrary// 调用methods中的函数  
      }],  
      // action sheet 默认不显示，为false。操作sheetVisible可以控制显示与隐藏  
      sheetVisible: false  
    }
  },
  methods:{
    actionSheet: function(){  
   // 打开action sheet  
      this.sheetVisible = true;  
    },  
    getCamera: function(){  
      console.log("打开照相机")  
    },  
    getLibrary: function(){  
      console.log("打开相册")  
    }  
  }

})

</script>
