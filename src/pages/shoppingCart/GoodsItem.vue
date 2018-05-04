<template>
  <section class="shopping-cart__goods-item-content">
      <div class="shopping-cart__goods-item-content-desc">A--food1</div>
      <Stepper class="shopping-cart__goods-item-content-stepper"/>
    </section>
</template>
<script>
import Stepper from "@/components/Stepper";
export default {
  name: "GoodsItem",
  components: {
    Stepper
  }
};
</script>
<style lang="less">
.shopping-cart__goods-item {
  &-content {
    display: flex;
    align-content: center;
    margin: 0 10px;
    padding: 15px 0;
    border-bottom: 1px solid #ccc;
    &-desc {
      flex: 1;
    }
    &-stepper {
      width: 100px;
    }
  }
}
</style>
