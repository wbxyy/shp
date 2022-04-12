<template>
  <header class="header">
    <!-- 顶条 -->
    <div class="top_bar">
      <div class="w">
        <div class="welcome">
          <div class="title">尚硅谷欢迎您！</div>
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
    </div>
    <!-- 底栏 -->
    <div class="wrap w">
      <div class="logo"><h1>尚品汇</h1></div>
      <div class="search">
        <input class="search_ipt" type="text" />
        <button class="search_btn">搜索</button>
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
<style lang="less" scoped>
.header {
  font-size: 12px;
  color: #676867;
}
.top_bar {
  background-color: #eaeaea;
  height: 30px;
  .w {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .w .welcome,
  .shortcut {
    line-height: 30px;
    height: 30px;
    display: flex;
  }

  .w .welcome .title {
    margin-right: 10px;
  }

  .w .shortcut ul {
    display: flex;
  }
  .w .shortcut ul li a {
    // display: inline-block;
    padding: 0 12px;
    border-right: 1px solid #b0b0b0;
  }
  .w .shortcut ul :last-child a {
    border-right: none;
  }
}

.wrap {
  padding-top: 30px;
  height: 240px;
  display: flex;
  justify-content: space-between;
  .logo {
    margin-left: 50px;

    h1 {
      margin: 0;
      width: 176px;
      height: 61px;
      text-indent: -9999px;
      background: url(./img/logo.png) no-repeat;
    }
  }
  .search {
    display: flex;
    border: 1px solid #e35e40;
    width: 702px;
    height: 42px;
    .search_ipt {
      height: 40px;
      width: 600px;
      padding-left: 12px;
      font-size: 16px;
    }

    .search_btn {
      height: 40px;
      line-height: 40px;
      width: 100px;
      background-color: #f75932;
      color: #fff;
      outline: none;
    }
  }
}
</style>
