<template>
  <div class="home">
    <div>
      <el-carousel :interval="2000" class="carouselContainer" arrow="always">
        <el-carousel-item>
          <div class="item">
            <img src="../assets/carouselImg/twoFinish.jpg" class="carouselImg" alt=""/>
          </div>
        </el-carousel-item>

        <el-carousel-item>
          <div class="item">
            <img src="../assets/carouselImg/imgOne.jpg" class="carouselImg" alt=""/>
          </div>
        </el-carousel-item>

        <el-carousel-item>
          <div class="item">
            <img src="../assets/carouselImg/imgTwo.jpg" class="carouselImg" alt=""/>
          </div>
        </el-carousel-item>

        <el-carousel-item>
          <div class="item">
            <img src="../assets/carouselImg/imgThree.jpg" class="carouselImg" alt=""/>
          </div>
        </el-carousel-item>

        <el-carousel-item>
          <div class="item">
            <img src="../assets/carouselImg/imgFour.jpg" class="carouselImg" alt=""/>
          </div>
        </el-carousel-item>

        <!--    <el-carousel-item>-->
        <!--      <div class="item">-->
        <!--        <img src="../assets/carouselImg/fourFinish.jpg" class="carouselImg" alt="" />-->
        <!--      </div>-->
        <!--    </el-carousel-item>-->
        <div class="layout"/>
      </el-carousel>
    </div>
    <hotel-info/>
    <div class="hotelCardsWrapper">
      <span class="cardsTitle">Номера</span>
      <hotel-cards/>
    </div>
    <footer-info/>
  </div>
</template>

<script>
import HotelInfo from '../components/hotelInfo.vue';
import HotelCards from '../components/hotelCards.vue';
import FooterInfo from '../components/footerInfo.vue';

export default {
  name: 'Home',
  components: {
    FooterInfo,
    HotelCards,
    HotelInfo,
  },
  data() {
    return {
      images: null,
      drawer: false,
    };
  },
};
</script>

<style lang="scss">
.el-carousel__container {
  height: 100vh !important;
}
@media (min-width: 1201px) and (max-width: 1500px) {
  .el-carousel__container {
    height: calc(53.5vw  + 150px) !important;
  }
}@media (min-width: 920px) and (max-width: 1199px) {
  .el-carousel__container {
    height: calc(50.5vw  + 150px) !important;
  }
}
@media (min-width: 760px) and (max-width: 919px) {
  .el-carousel__container {
    height: calc(40.5vw  + 150px) !important;
  }
}
@media (min-width: 412px) and (max-width: 759px) {
  .el-carousel__container {
    height: calc(30.5vw  + 150px) !important;
  }
}
@media (max-width: 413px) {
  .el-carousel__container {
    height: calc(20.5vw  + 150px) !important;
  }
}

.carouselImg {
  width: 100%;
}

.layout {
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(0 0 0 / 34%);
  z-index: 50;
}

.test {
  height: 1000px;
}

.el-carousel__arrow {
  z-index: 100 !important;
}
.el-drawer__body {
  background: radial-gradient(circle, #1f2827 0%, #2e3c4a 100%) !important;
}

.hotelInfo {
  padding: 20px;
}

.text {
  display: flex;
  font-size: 17px;
  flex-flow: column;
  align-items: baseline;
  font-weight: 300;
}

.textTwo {
  display: flex;
  flex-flow: column;
  font-weight: 300;
}

.title {
  font-size: 30px;
  font-weight: bold;
}

.hotelCardsWrapper {
  display: flex;
  flex-flow: column;
  align-items: center;
  //height: 30px;
}

.cardsTitle {
  font-size: 30px;
  font-family: Montserrat;
  font-weight: bold;
  margin-bottom: 40px;
}
</style>
