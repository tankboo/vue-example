<template>
  <div class="shopping-cart__cart">
      <div class="shopping-cart__cart-info">
          <div class="cart-img-warp">
              <div class="cart-img"></div>
              <sup class="cart-sup">10</sup>
          </div>
      </div>
      <button class="shopping-cart__cart-btn">
          去结算
      </button>
  </div>
</template>
<script>
export default {
  name: "Cart"
};
</script>
<style lang="less">
.shopping-cart {
  &__cart {
    position: fixed;
    left: 0;
    bottom: 0;
    right: 0;
    height: 3rem;
    background-color: #757171;
    display: flex;
    &-info {
      flex: 1;
      position: relative;
      .cart-img-warp {
        width: 48px;
        height: 48px;
        border-radius: 50%;
        position: absolute;
        padding: 10px;
        left: 20px;
        top: -10px;
        background-color: #757171;
        .cart-img {
        display: inline-block;
          text-align: center;
          height: 48px;
          width: 48px;
          border-radius: 50%;
          background-color: #fff;
          background-repeat: no-repeat;
          background-size: cover;
          background-position: -3px 2px;
          background-image: url("../../assets/images/shopping_cart.svg");
        }
        .cart-sup{
            position: absolute;
            top:8px;
            left: 40px;
            display: inline-block;
            background-color: deepskyblue;
            width: 20px;
            height: 20px;
            text-align: center;
            color: #fff;
            border-radius: 50%;
        }
      }
    }
    &-btn {
      width: 6rem;
      background-color: deepskyblue;
      color: #fff;
      border: none;
    }
  }
}
</style>
