<template>
  <div id="app">
  <router-view></router-view>
     <TarBar>
        <TarBarItem path="/home">
            <img slot="item-icon" src="./assets/img/tarbar/shouye.png" alt="">
            <img slot="item-icon-active" src="./assets/img/tarbar/main.png" alt="">
            <div slot="item-text" >首页</div>
        </TarBarItem>
        <TarBarItem path="/category">
            <img slot="item-icon" src="./assets/img/tarbar/fenlei.png" alt="">
            <img slot="item-icon-active" src="./assets/img/tarbar/category.png" alt="">
            <div slot="item-text" >分类</div>
        </TarBarItem>
        <TarBarItem path="/cart">
            <img slot="item-icon" src="./assets/img/tarbar/gouwuche.png" alt="">
            <img slot="item-icon-active" src="./assets/img/tarbar/cart.png" alt="">
            <div slot="item-text" >购物车</div>
        </TarBarItem>
        <TarBarItem path="/profile">
            <img slot="item-icon" src="./assets/img/tarbar/wode.png" alt="">
            <img slot="item-icon-active" src="./assets/img/tarbar/profile.png" alt="">
            <div slot="item-text" >我的</div>
        </TarBarItem>
     </TarBar>
  </div>
</template>

<script>
import TarBar from './components/tarbar/TarBar'
import TarBarItem from './components/tarbar/TabBarItem'
export default {
  name: 'App',
  components:{
    TarBar,
    TarBarItem
  }
}
</script>

<style>
  @import "./assets/css/base.css";
</style>
