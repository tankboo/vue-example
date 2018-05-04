<template>
  <div class="header">
      <h4>{{title}}</h4>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: {
    title: {
      type: String,
      required: true
    }
  }
};
</script>
<style lang="less">
.header {
  background-color: deepskyblue;
  padding: 1rem;
}
.header h4 {
  color: #fff;
  text-align: center;
}
</style>

