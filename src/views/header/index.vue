<template>
  <div>
    <h3>{{ title }}</h3>
    <button @click="watchHeaden">监听父组件事件</button>
  </div>
</template>
<script>
export default {
  name: "HeaderPage",
  props: {
    //通过props 向子组件传值
    title: String,
  },
  data() {
    //数据层
    return {};
  },
  methods: {
    watchHeaden() {
      this.$emit("watchHeade",'你好'); //this.$emit('父组件监听方法名',子组件传给父组件的值。父组件函数可通过方法中的第一个参数获取)
    },
  },
};
</script>
<style lang="less" scoped>
</style>