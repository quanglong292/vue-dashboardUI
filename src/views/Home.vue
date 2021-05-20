<template>
  <div id="layout">
    <a-layout class="myLayout">
      <a-drawer
        :placement="placement"
        closable
        :visible="visible"
        @close="onClose"
        id="test"
      >
        <h1 class="dashboard-header">
          <span class="dashboard-logo">D</span>
          Dashboard
        </h1>
        <div class="dashboard-router">
          <a><a-icon type="user" /> Dashboard</a>
          <a><a-icon type="question-circle" /> Calendar</a>
          <a><a-icon type="minus-square" /> Stats</a>
        </div>
        <div class="dashboard-login">
          <a><a-icon type="login" /> Login</a>
        </div>
      </a-drawer>

      <a-layout>
        <a-layout-header>
          <a-button type="default" size="large" @click="showDrawer">
            <a-icon type="menu" />
          </a-button>
          <a-input-search placeholder="Search..." class="nav-search" />
          <div class="user-logo">
            <span class="user-title">Mr. Oscar</span>
            <a-badge dot><a-avatar icon="user" :size="50" /></a-badge>
          </div>
        </a-layout-header>
        <a-layout-content>
          <Content :Charge="Charge"/>
          <BodyContent :Charge="Charge"/>
        </a-layout-content>
      </a-layout>
    </a-layout>
    <div>
      <a-back-top />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Vue from "vue";
import { Button, Icon, Layout, Row } from "ant-design-vue";
Vue.use(Button, Icon, Layout, Row);
import Content from "../components/Content";
import BodyContent from "../components/BodyContent";
import Charge from "../../src/assets/chart.png";

export default {
  name: "Home",
  components: { Content, BodyContent},
  data() {
    return {
      visible: false,
      placement: "left",
      Charge
    };
  },
  methods: {
    showDrawer() {
      this.visible = true;
    },
    onClose() {
      this.visible = false;
    },
    onChange(e) {
      this.placement = e.target.value;
    },
  },
};
</script>

<style lang="scss" scoped>
.dashboard-header {
  font-size: 20px;
  color: #8ed5fc;
  font-weight: 700;
  .dashboard-logo {
    // width: 50px;
    // height: 50px;
    padding: 10px 13px;
    border-radius: 50%;
    background: #8ED5FC;
    font-size: 20px;
    font-weight: 700;
    color: white;
    margin-right: 10px;
  }
}
.dashboard-router {
  a {
    i {
      margin-right: 15px;
    }
    display: block;
    color: rgb(145, 140, 140);
    font-size: 16px;
    font-weight: 400;
    margin: 20px;
    margin-top: 30px;
    transition: 0.3s;
    &:hover {
      color: rgb(53, 73, 94);
    }
  }
}
.dashboard-login {
  position: absolute;
  bottom: 20px;
  left: 20px;
  a {
    i {
      margin-right: 15px;
    }
    display: block;
    color: rgb(145, 140, 140);
    font-size: 16px;
    font-weight: 400;
    margin: 20px;
    margin-top: 30px;
    transition: 0.3s;
    &:hover {
      color: rgb(53, 73, 94);
    }
  }
}
.ant-input-search {
  width: 50%;
  margin-left: 200px;
}
.nav-search {
  .ant-input {
    height: 40px;
    padding: 6px 20px;
  }
}
.user-logo {
  position: absolute;
  right: 30px;
  top: -3px;
  .user-title {
    color: white;
    margin-right: 10px;
    font-weight: 700;
    cursor: pointer;
    transition: 0.3s;
    &:hover {
      color: #259FFB;
    }
  }
}
</style>
