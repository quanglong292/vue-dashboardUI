<template>
  <div class="bodycontent-container">
    <a-row type="flex" justify="space-between">
      <a-col>
        <div class="mycard">
          <a-row type="flex" justify="space-between" class="mycard-content">
            <h1>Quick Overview</h1>
            <div>
              <p>+2,562</p>
              <p>Lorem ipsum</p>
            </div>
          </a-row>
          <img :src="Charge" alt="" width="430" height="600" class="chart" />
        </div>
      </a-col>
      <a-col>
        <div class="right-cards">
          <div class="right-card">
            <a-row type="flex" justify="space-between" class="right-card-content">
              <h1>Lorem ipsum</h1>
              <div>
                <a-icon type="exclamation-circle" theme="twoTone"/>
                <a-icon type="info-circle" />
                <a-time-picker use12-hours @change="onChange" />
              </div>
            </a-row>
            <img
              :src="ChartBig"
              alt=""
              width="800"
              height="330"
              class="chart"
            />
          </div>
          <div class="right-card right-bottom-card">
              <div class="verticle-line"></div>
              <a-row type="flex" align="middle" class="bottom-card-content">
                  <a-col :span="18">
                      <h1>Lorem ipsum</h1>
                      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eligendi tempore explicabo velit, perspiciatis dicta odio quas est ratione doloremque veritatis sunt asperiores eius autem quidem. Dignissimos quasi porro, rem cumque suscipit placeat ipsum aperiam veniam nisi, ratione, repellendus nostrum omnis!</p>
                  </a-col>
                  <a-col :span="4">
                      <a-button type="primary">Lorem, ipsum.</a-button>
                  </a-col>
              </a-row>
          </div>
        </div>
      </a-col>
    </a-row>
  </div>
</template>

<script>
import ChartBig from "../assets/chart-big.png";

export default {
  name: "BodyContent",
  data() {
    return {
      ChartBig,
    };
  },
  props: {
    Charge: String,
  },
};
</script>

<style lang="scss" scoped>
.bodycontent-container {
  max-width: 1440px;
  height: 100%;
  margin: 0 auto;
  .mycard {
    width: 500px;
    height: 700px;
    background: #fafafa;
    position: relative;
    box-shadow: 2px 0 5px rgba(94, 93, 93, 0.3);
    border-radius: 20px;
    padding: 20px;
    .mycard-content {
      h1 {
        font-size: 25px;
        font-weight: 700;
        color: #575757;
      }
      div {
        text-align: center;
        p {
          margin: 0;
          font-size: 25px;
          font-weight: 700;
          color: #b1e0f9;
          &:last-child {
            font-size: 15px;
          }
        }
      }
    }
    .chart {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 0);
    }
  }

  .right-cards {
    width: 50%;
    height: 700px;
    .right-card {
      width: 900px;
      height: 450px;
      background: #fafafa;
      border-radius: 10px;
      position: relative;
      box-shadow: 2px 0 5px rgba(94, 93, 93, 0.3);
      padding: 20px;
      .right-card-content {
          i {
              font-size: 25px;
              margin: 0 10px;
              cursor: pointer;
          }
      }
      h1 {
        font-size: 25px;
        font-weight: 700;
        color: #575757;
      }
      img {
        position: absolute;
        bottom: 10%;
        left: 50%;
        transform: translate(-50%, 0);
      }
    }
    .right-bottom-card {
        background: rgb(23, 24, 44);
        margin-top: 25px;
        height: 220px;
        .verticle-line {
            position: absolute;
            width: 5px;
            height: 100%;
            top: 0;
            left: 0;
            background: #259FFB;
            padding: 5px;
            border-radius: 10px 0 0 10px;
        }
        .bottom-card-content {
            height: 100%;
            margin-left: 20px;
            color: white;
            h1 {
                color: #259FFB;
            }
            p {
                padding-right: 40px;
            }
        }
    }
  }
}
</style>