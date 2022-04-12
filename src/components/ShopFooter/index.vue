<template>
  <footer></footer>
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
