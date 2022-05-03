<template>
  <div>
    <!-- 头部 -->
    <header>
      <HeaderPage
        ref="headerPage"
        :title="HeaderTitle.title"
        @watchHeade="watchTitle"
      ></HeaderPage>
    </header>
    <!-- 主体内容部分 -->
    <main><MainPage ref="mainPage" :title="MainTitle.title"></MainPage></main>
    <!-- 尾部 -->
    <footer>
      <FooterPage ref="footerPage" :title="FooterTitle.title"></FooterPage>
    </footer>
  </div>
</template>
<script>
export default {
  name: "Home",
  data() {
    //数据层
    return {
      HeaderTitle: {
        title: "头部内容",
      },
      MainTitle: {
        title: "主体内容部分",
      },
      FooterTitle: {
        title: "尾部内容",
      },
    };
  },
  components: {
    //复用组件
    HeaderPage: () => import("./views/header/index.vue"), //网页头部组件
    MainPage: () => import("./views/main/index.vue"), //网页主体内容组件
    FooterPage: () => import("./views/footer/index.vue"), //网页尾部内容组件
  },
  computed: {
    //变量监听计算属性
  },
  watch: {
    //监听 事件和变量
  },
  methods: {
    //方法层
    watchTitle(ev){
      this.HeaderTitle.title='头部内容进行修改'+ev
    }
  },
};
</script>
<style lang="less" scoped>
</style>