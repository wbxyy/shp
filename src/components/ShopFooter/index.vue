<template>
  <header>
    <!-- 顶条 -->
    <div class="top_bar">
      <div class="welcome">
        <div class="title">尚硅谷欢迎您</div>
        <div class="login">
          <span>请登录</span>
          |
          <span>免费注册</span>
        </div>
      </div>
      <div class="shortcut">
        <ul>
          <li v-for="(item, index) in shortcut">
            <a href="#">{{ item.title }}</a>
          </li>
        </ul>
      </div>
    </div>
    <!-- 底栏 -->
    <div class="wrap">
      <div class="logo"><h1></h1></div>
      <div class="search">
        <input type="search" />
      </div>
    </div>
  </header>
</template>
<script>
import { defineComponent } from 'vue'
export default defineComponent({
  data() {
    return {
      shortcut: [{ title: '我的订单' }, { title: '我的购物车' }, { title: '我的尚品汇' }, { title: '尚品汇会员' }, { title: '企业采购' }, { title: '关注尚品汇' }, { title: '合作招商' }, { title: '商家后台' }],
    }
  },
})
</script>
<style lang="less" scoped></style>
