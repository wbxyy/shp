<template>
  <ShopHeader></ShopHeader>
  <ShopFooter></ShopFooter>
</template>
<script>
import { defineComponent } from 'vue'
import ShopHeader from './components/ShopHeader'
import ShopFooter from './components/ShopFooter'
export default defineComponent({
  components: {
    ShopHeader,
    ShopFooter,
  },
  data() {
    return {}
  },
})
</script>
<style lang="less" scoped></style>
