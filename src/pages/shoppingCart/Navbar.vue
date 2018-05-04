<template>
  <ul class="shopping-cart__nav-bar">
    <li 
        class="shopping-cart__nav-bar-item"
        v-for="(item, index) in items" 
        :class="index==menuCurrentIndex?'item-selected':''"
        :key="item.id"
        @click="clickHandle(item, index)"
    >{{item.name}}</li>
  </ul>
</template>
<script>
export default {
  name: "Navbar",
  data() {
    return {
      menuCurrentIndex: 0
    };
  },
  computed: {
    items() {
      let items = [];
      for (let i = 65; i < 91; i++) {
        const item = {
          id: i ,
          name: String.fromCharCode(i)
        };
        items.push(item);
      }
      return items;
    }
  },
  methods: {
    clickHandle(item, index) {
      if (index !== this.menuCurrentIndex) {
        this.menuCurrentIndex = index;
        console.log(JSON.stringify(item));
      }
    }
  }
};
</script>
<style lang="less">
.shopping-cart {
  &__nav-bar {
    width: 5rem;
    background-color: #518cbb;
    color: #fff;
    overflow:auto;
    &-item {
      padding: 0.6rem 0;
      text-align: center;
      border-bottom: 1px solid #ccc;
    }
    .item-selected {
      background-color: #fff;
      color: #518cbb;
    }
  }
}
</style>
