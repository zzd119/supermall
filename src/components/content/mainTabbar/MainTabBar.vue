<template>
      <tab-bar>
        <tab-bar-item path='/home'><div slot="item-text">首页</div></tab-bar-item>
        <tab-bar-item path='/category'><div slot="item-text">分类</div></tab-bar-item>
        <tab-bar-item path='/cart'><div slot="item-text">购物车</div></tab-bar-item>
        <tab-bar-item path='/profile'><div slot="item-text">我的</div></tab-bar-item>
      </tab-bar>
</template>
<script>
import TabBar from "components/common/tabbar/TabBar.vue"
import TabBarItem from "components/common/tabbar/TabBarItem.vue"
export default {
    name: "MainTabBar",
    components:{
      TabBar,
      TabBarItem
    }
}
</script>

<style>

</style>
