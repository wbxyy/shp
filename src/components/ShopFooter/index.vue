<template>
  <footer class="footer">
    <div class="help w">
      <div v-for="(help, index) in helps" :key="index">
        <dl>
          <dt>{{ help.title }}</dt>
          <dd v-for="(item, index) in help.list" :key="index">
            {{ item }}
          </dd>
        </dl>
      </div>
      <div>
        <dl>
          <dt>帮助中心</dt>
          <dd><img src="./img/wx_cz.jpg" alt="" /></dd>
        </dl>
      </div>
    </div>
    <div class="links">
      <ul>
        <li v-for="(item, index) in links" :key="index">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
      <div class="address">地址：{{ address }}</div>
      <div class="beian">京ICP备19006430号</div>
    </div>
  </footer>
</template>
<script>
import { defineComponent } from 'vue'
export default defineComponent({
  data() {
    return {
      helps: [
        { title: '购物指南', list: ['购物流程', '会员介绍', '生活旅行/团购', '常见问题', '购物指南'] },
        { title: '购物指南', list: ['购物流程', '会员介绍', '生活旅行/团购', '常见问题', '购物指南'] },
        { title: '购物指南', list: ['购物流程', '会员介绍', '生活旅行/团购', '常见问题', '购物指南'] },
        { title: '购物指南', list: ['购物流程', '会员介绍', '生活旅行/团购', '常见问题', '购物指南'] },
        { title: '购物指南', list: ['购物流程', '会员介绍', '生活旅行/团购', '常见问题', '购物指南'] },
      ],
      links: ['关于我们', '联系我们', '商家入驻', '营销中心', '友情链接', '关于我们', '联系我们', '商家入驻', '营销中心', '友情链接'],
      address: '北京市昌平区宏福科技园综合楼6层',
    }
  },
})
</script>
<style lang="less" scoped>
.footer {
  font-size: 12px;
  padding-top: 30px;
  background-color: #eaeaea;
}

.help {
  display: flex;
  justify-content: space-between;
  dl dt {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 700;
  }

  dl dd {
    font-size: 14px;
    line-height: 1.35;
  }
}

.links {
  padding-top: 30px;
  padding-bottom: 30px;
  border-top: 1px solid #e3e3e3;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  & > * {
    margin-top: 12px;
  }
  ul {
    display: flex;
  }
  ul li a {
    padding: 0 12px;
    border-right: 1px solid #b0b0b0;
  }
}
</style>
