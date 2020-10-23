<template>
  <tab-bar class="tab-bar">
    <tab-bar-item v-once path="/home">
      <img slot="slot-icon" src="~assets/img/home/home.png" alt="">
      <img slot="slot-icon-active" src="~assets/img/home/home-active.png" alt="">
      <div slot="slot-text">主页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <img slot="slot-icon" src="~assets/img/category/category.png" alt="">
      <img slot="slot-icon-active" src="~assets/img/category/category-active.png" alt="">
      <div slot="slot-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="slot-icon" src="~assets/img/cart/cart.png" alt="">
      <img slot="slot-icon-active" src="~assets/img/cart/cart-active.png" alt="">
      <div slot="slot-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="slot-icon" src="~assets/img/profile/profile.png" alt="">
      <img slot="slot-icon-active" src="~assets/img/profile/profile-active.png" alt="">
      <div slot="slot-text">个人中心</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
  import TabBar from 'components/common/tabbar/TabBar'
  import TabBarItem from 'components/common/tabbar/TabBarItem'

  export default {
    name: "main-tab-bar",
    components: {
      TabBar,
      TabBarItem
    }
  }
</script>

<style scoped>
  .tab-bar {
    position: fixed;
  }

</style>
