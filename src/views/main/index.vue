<template>
    <div>
       {{title}}
    </div>
</template>
<script>
export default {
name:'MainPage',
props:{
//通过props 向子组件传值
title:String,
},
data() {
    //数据层
    return {
        
    }
},
}
</script>
<style lang="less" scoped>

</style>