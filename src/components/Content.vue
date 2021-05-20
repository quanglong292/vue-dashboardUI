<template>
  <div class="content-container">
    <a-row type="flex" justify="space-between">
      <a-col :span="[24, { md: 8 }]">
        <div class="myCard">
          <div class="card-charge">
            <span class="charge-dot"></span>
            <img :src="Charge" alt="" width="300" />
          </div>
          <div class="card-content">
            <div class="card-script">Daily Stats</div>
            <div class="card-divider">
              <a-divider type="vertical" />
            </div>
            <div class="card-stats-result">
              <p>+1,532</p>
              <p>Lorem ipsum</p>
            </div>
          </div>
        </div>
      </a-col>
      <a-col :span="[24, { md: 8 }]">
        <div class="myCard">
          <div class="card-charge">
            <span class="charge-dot"></span>
            <img :src="Charge" alt="" width="300" />
          </div>
          <div class="card-content">
            <div class="card-script">Daily Stats</div>
            <div class="card-divider">
              <a-divider type="vertical" />
            </div>
            <div class="card-stats-result">
              <p>+1,532</p>
              <p>Lorem ipsum</p>
            </div>
          </div>
        </div>
      </a-col>
      <a-col :span="[24, { md: 8 }]">
        <div class="myCard">
          <div class="card-charge">
            <span class="charge-dot"></span>
            <img :src="Charge" alt="" width="300" />
          </div>
          <div class="card-content">
            <div class="card-script">Daily Stats</div>
            <div class="card-divider">
              <a-divider type="vertical" />
            </div>
            <div class="card-stats-result">
              <p>+1,532</p>
              <p>Lorem ipsum</p>
            </div>
          </div>
        </div>
      </a-col>
    </a-row>
  </div>
</template>

<script>

export default {
  name: "Content",
  data() {
    return {
      
    };
  },
  props: {
    Charge: String
  }
};
</script>

<style lang="scss" scoped>
.content-container {
  max-width: 1440px;
  margin: 30px auto;
  margin-top: 30px;
  .justify-cards {
    justify-content: space-evenly;
  }
}
.myCard {
  position: relative;
  background: #fafafa;
  width: 400px;
  height: 300px;
  box-shadow: 2px 0 5px rgba(94, 93, 93, 0.3);
  border-radius: 20px;
  margin: 20px 10px;
  .card-charge {
    position: absolute;
    bottom: 35px;
    left: 10px;
    img {
      border-radius: 0 0 0 20px;
    }
    .charge-dot {
      position: absolute;
      top: -28px;
      left: 8px;
      padding: 5px;
      border-radius: 50%;
      background: #B1E0F9;
      cursor: pointer;
      transition: 0.3s;
      &:hover {
        background: #60b82c;
      }
    }
  }
  .card-content {
    position: absolute;
    top: 10px;
    right: 25px;
    .card-script {
      font-size: 17px;
      font-weight: 700;
      text-align: center;
      margin-bottom: 10px;
    }
    .card-divider {
      text-align: center;
    }
    .card-stats-result {
      text-align: center;
      p {
        margin: 0;
        margin-top: 10px;
        font-size: 20px;
        font-weight: 700;
        color: #B1E0F9;
        &:last-child {
          font-size: 13px;
          margin: 0;
        }
      }
    }
  }
}
</style>