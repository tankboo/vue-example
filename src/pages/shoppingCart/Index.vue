<template>
  <div class="warp">
    <Header title="仿饿了么购物车"/>
    <div class="shopping-cart">
      <NavBar/>
      <div class="shopping-cart__list">
        <GoodsList/>
        <GoodsList/>
        <GoodsList/>
        <GoodsList/>
      </div>
    </div>
    <Cart/>
  </div>
</template>
<script>
import Header from "@/components/Header";
import NavBar from "./NavBar";
import Cart from "./Cart";
import GoodsList from "./GoodsList"
export default {
  name: "ShoppingCart",
  components: {
    Header,
    NavBar,
    Cart,
    GoodsList
  }
};
</script>
<style lang="less">
.shopping-cart {
  display: flex;
  position: fixed;
  top: 54px;
  left: 0;
  right: 0;
  bottom: 3rem;
  &__list {
    flex: 1;
    overflow-x: hidden;
    overflow-y: auto;
  }
}
</style>
