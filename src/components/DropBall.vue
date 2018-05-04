<template>
    <transition name="fade">
        <div class="ball-container">
            <div class="ball"></div>
        </div>
    </transition>
</template>
<script>
export default {
  name: "DropBall",
  data() {
    return {
      datas: [
        {
          show: false
        },
        {
          show: false
        }
      ]
    };
  }
};
</script>
<style lang="less">
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>
