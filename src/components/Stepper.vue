<template>
  <div class="stepper " :class="classObjcet">
      <button class="stepper-btn popSub" :class="{ mov: value>0}" @click.stop.prevent="decrease">-</button>
      <span class="text popText" :class="{ mov: value>0}">{{value}}</span>
      <button class="stepper-btn" @click.stop.prevent="add">+</button>
  </div>
</template>
<script>
export default {
  name: "Stepper",
  props: {
    min: {
      type: Number
    },
    defaultValue: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      value: this.defaultValue
    };
  },
  computed: {
    classObjcet() {
      return this.value > 0 ? "showCount" : "";
    }
  },
  methods: {
    decrease(e) {
      this.value = this.value - 1 > 0 ? this.value - 1 : 0;
    },
    add(e) {
      //console.log({ e });
      const top = e.clientY;
      const left = e.clientX;
      const endTop = window.innerHeight - 30; // 小球降落终点
      const endLeft = 20;

      console.log({ left, top, endLeft, endTop });
      this.value = this.value + 1 > 0 ? this.value + 1 : 0;
    }
  }
};
</script>
<style lang="less">
.stepper {
  color: #518cbb;
  text-align: right;
  .text {
    width: 25px;
    display: inline-block;
    text-align: center;
    position: relative;
  }
  .stepper-btn {
    padding: 1px 2px;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    background-color: deepskyblue;
    color: #fff;
    box-sizing: border-box;
    outline: none;
    position: relative;
  }
  .popSub {
    opacity: 0;
    left: 56px;
  }
  .popText {
    opacity: 0;
    left: 56px;
  }
  .mov {
    left: 0;
    opacity: 1;
    transition: all ease 0.5s;
    animation: stepperMove 0.5s;
  }
  @keyframes stepperMove {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }
}
</style>
