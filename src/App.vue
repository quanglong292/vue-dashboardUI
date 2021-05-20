<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
import Vue from "vue";
import Antd from "ant-design-vue";
import "ant-design-vue/dist/antd.css";

Vue.use(Antd);
export default {};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.ant-drawer .ant-drawer-header {
  border-bottom: none;
}
.ant-layout-header {
  background: #C7DDE7;
}
.ant-input {
  height: 40px;
  padding: 6px 20px;
  border-radius: 100px;
}
.ant-badge-dot {
  background: rgb(65, 184, 131);
}
.ant-layout-content {
  background: white;
}
.ant-divider, .ant-divider-vertical {
  height: 13.0em;
  width: 2px;
}
</style>
