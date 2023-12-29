<template>
  <div class="bgc">
    <headerNav></headerNav>
    <div class="content">
      <p class="name">Eddie Tsai</p>
      <p class="title">FRONTEND SOFTWARE ENGINEER</p>
      <p class="hobbies">#Traveling #Camping #Movies #Drama #Fitness #Programming
      </p>
      <div class="skills">
        <a href="https://google.com">
          <v-icon class="mr-5 icon ">mdi-facebook</v-icon>
        </a>
        <a href="https://google.com">
          <v-icon class="mr-5 icon ">mdi-instagram</v-icon>
        </a><a href="https://google.com">
          <v-icon class="mr-5 icon ">mdi-github</v-icon>
        </a>
      </div>
    </div>
  </div>
</template>


<script setup>
import headerNav from './headerCom.vue'
</script>
<style lang="scss" scoped>
.bgc {
  background-image: url('https://images.pexels.com/photos/2775196/pexels-photo-2775196.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2') !important;
  background-size: cover;
  min-height: 100vh;
  width: 100vw;
  position: relative;
}

.content {
  position: absolute;
  width: 60%;
  left: 50%;
  transform: translateX(-50%);
  margin-top: 150px;
  padding-top: 20px;
  /* 調整內容與上方的間距 */
  // background: rgba(255, 255, 255, 0.8);
  /* 為內容區域添加背景色 */
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  height: 300px;

  .name {
    font-size: 80px;
    color: white;
    font-weight: 900;
    letter-spacing: 3px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  }

  .title {
    font-size: 16px;
    color: white;
    letter-spacing: 2px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  }

  .hobbies {
    margin-top: 15px;
    font-size: 16px;
    color: #F1E2C8;
    letter-spacing: 2px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  }

  .skills {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: center;
    margin-top: 30px;

    .icon {
      color: white;
      font-size: 40px;
    }
  }
}
</style>
