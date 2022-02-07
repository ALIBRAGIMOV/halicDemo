<template>
  <div class="hotelCardsContainer">
    <div class="hotelCardContainer">
      <img style="width: 100%; height: 265px;
     border-top-right-radius: 24px; border-top-left-radius: 24px;" src="../assets/hotelCardImg.jpg">
      <span style="padding-top: 1rem" class="cardsTitle">
      ДВУХМЕСТНЫЙ НОМЕР
    </span>
      <div class="cardInfoWrapper">
      <span class="cardsInfoText">
        🟤 1 КОМНАТА
      </span>
        <span class="cardsInfoText">
       🟤 ВАННАЯ
      </span>
        <span class="cardsInfoText">
        🟤 ХОЛОДИЛЬНИК
      </span>
        <span class="cardsInfoText">
       🟤 КОНДИЦИОНЕР
      </span>
        <span class="cardsInfoText">
        🟤 ТЕЛЕВИЗОР
      </span>
      </div>
      <div class="costWrap">
        <span>4000₽</span>
      </div>
    </div>
    <div class="hotelCardContainer">
      <el-carousel
        style="width: 100%;
      border-top-left-radius: 24px;
       border-top-right-radius: 24px;"
                   height="280px !important" :interval="5000" arrow="always">
        <el-carousel-item>
          <div class="item">
            <el-image
              class="carouselImg"
              :src="url"
              :preview-src-list="srcList">
            </el-image>
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div class="item">
            <el-image
              class="carouselImg"
              :src="urlTwo"
              :preview-src-list="srcListTwo">
            </el-image>
          </div>
        </el-carousel-item>
      </el-carousel>
      <!--      <el-carousel style="width: 100%; height: 35%;-->
      <!--     border-top-right-radius: 24px; border-top-left-radius: 24px;">-->
      <!--      </el-carousel>-->
      <span class="cardsTitle">
      ТРЕХМЕСТНЫЙ НОМЕР
    </span>
      <div class="cardInfoWrapper">
      <span class="cardsInfoText">
        🟤 2 КОМНАТЫ
      </span>
        <span class="cardsInfoText">
       🟤 ВАННАЯ
      </span>
        <span class="cardsInfoText">
        🟤 ХОЛОДИЛЬНИК
      </span>
        <span class="cardsInfoText">
       🟤 КОНДИЦИОНЕР
      </span>
        <span class="cardsInfoText">
        🟤 ТЕЛЕВИЗОР
      </span>
      </div>
      <div class="costWrap">
        <span>4000₽</span>
      </div>
    </div>
    <div class="hotelCardContainer">
      <el-carousel
        style="width: 100%;
      border-top-left-radius: 24px;
       border-top-right-radius: 24px"
        height="280px !important" :interval="5000" arrow="always">
        <el-carousel-item>
          <div class="item">
            <el-image
              class="carouselImg"
              :src="urlThree"
              :preview-src-list="srcListThree">
            </el-image>
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div class="item">
            <el-image
              class="carouselImg"
              :src="urlFour"
              :preview-src-list="srcListFour">
            </el-image>
          </div>
        </el-carousel-item>
      </el-carousel>
      <span class="cardsTitle">
      ЧЕТЫРЕХМЕСТНЫЙ НОМЕР
    </span>
      <div class="cardInfoWrapper">
      <span class="cardsInfoText">
        🟤 2 КОМНАТЫ
      </span>
        <span class="cardsInfoText">
       🟤 ВАННАЯ
      </span>
        <span class="cardsInfoText">
        🟤 ХОЛОДИЛЬНИК
      </span>
        <span class="cardsInfoText">
       🟤 КОНДИЦИОНЕР
      </span>
        <span class="cardsInfoText">
        🟤 ТЕЛЕВИЗОР
      </span>
      </div>
      <div class="costWrap">
        <span>4000₽</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hotelCards',
  data() {
    return {
      // eslint-disable-next-line global-require
      url: require('../assets/carouselHotel/hotelCarSix.jpg'),
      // eslint-disable-next-line global-require
      urlTwo: require('../assets/carouselHotel/hotelCarFive.jpg'),
      // eslint-disable-next-line global-require
      urlThree: require('../assets/carouselHotel/hotelCarFour.jpg'),
      // eslint-disable-next-line global-require
      urlFour: require('../assets/carouselHotel/hotelCarThree.jpg'),
      srcList: [
        // eslint-disable-next-line global-require
        require('../assets/carouselHotel/hotelCarSix.jpg'),
      ],
      srcListTwo: [
        // eslint-disable-next-line global-require
        require('../assets/carouselHotel/hotelCarFive.jpg'),
      ],
      srcListThree: [
        // eslint-disable-next-line global-require
        require('../assets/carouselHotel/hotelCarFour.jpg'),
      ],
      srcListFour: [
        // eslint-disable-next-line global-require
        require('../assets/carouselHotel/hotelCarThree.jpg'),
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com");
@import url("https://fonts.gstatic.com");
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600&display=swap");

.hotelCardsContainer {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  width: 100%;
  justify-content: space-around;
}

.hotelCardContainer {
  background: #ffffff;
  border-radius: 24px;
  display: flex;
  margin: 20px 0;
  flex-direction: column;
  font-weight: 600;
  align-items: center;
  //justify-content: space-between;
  width: 17rem;
  height: 522px;
  cursor: pointer;
  transition-duration: .3s;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  font-family: Montserrat;
}
//@media (max-width: 768px) {
//  .hotelCardContainer{
//    width: 10rem;
//    height: 200px;
//    font-size: 10px;
//  }
//}

//.hotelCardContainer:hover {
//  box-shadow: none;
//  border: 0.3px solid rgba(128, 108, 108, 0.65);
//}

.cardsTitle {
  font-size: 1rem;
  font-weight: bold;
}

.cardsWrapper {
  background: url(../assets/hotelCardImg.jpg);
  border-radius: 24px;
}

.cardInfoWrapper {
  display: flex;
  align-items: flex-start;
  flex-flow: column;
  width: 100%;
  padding-left: 3rem;
  margin-top: 10px;
}

.cardsInfoText {
  font-weight: 300;
  font-size: 16px;
}

.costWrap {
  display: flex;
  width: 100%;
  justify-content: end;
  padding-right: 3rem;
}
.carouselImg{
  width: 100%;
  height: 265px;
}
</style>
