<template>
  <div class="shopping-cart__goods-item">
    <div class="shopping-cart__goods-item-title">A</div>
    <GoodsItem/>
    <GoodsItem/>
    <GoodsItem/>
  </div>
</template>
<script>
import GoodsItem from "./GoodsItem";
export default {
  name: "GoodsList",
  components: {
    GoodsItem
  }
};
</script>
<style lang="less">
.shopping-cart__goods-item {
  &-title {
    padding: 7px 20px;
    background-color: lightgrey;
    font-size: 20px;
    color: #fff;
    margin-top: -1px;
  }
}
</style>
