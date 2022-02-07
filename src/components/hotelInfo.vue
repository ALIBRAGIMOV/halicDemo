<template>
  <div class="hotelInfo">
    <span class="title">Об Отеле</span>
    <div class="hotelInfoWrapper">
      <div class="hotelInfoText">
        <div class="">
          <img style="width: 30px; background: #F0BB1F; padding: 13px; border-radius: 20px;"
               src="../assets/hotel.svg">
          <div class="hotelInfoTextsWrapper">
            <span class="hotelInfoTitle">Отель</span>
            <span class="hotelInfoTexts">
            Причал - расположен в одном из самых живописных уголков
              <br/>
          Дагестана, на берегу Каспийского моря
              в 20км от международного Аэропорта "Уйташ" Махачкала.
          </span>
          </div>
        </div>
      </div>
      <div style="margin: 40px 0 40px 0" class="hotelInfoText">
        <div class="">
          <img style="width: 50px" src="../assets/beach.svg">
          <div class="hotelInfoTextsWrapper">
            <span class="hotelInfoTitle">Номера</span>
            <span class="hotelInfoTexts">
              В номерном фонде отели 3 категории комфортабельных номеров. Номера
              <br/>
            оснащены всем необходимым для комфортного время препровождения и
              <br/>
            отличного отдыха.
          </span>
          </div>
        </div>
      </div>
      <div class="hotelInfoText">
        <div class="">
          <img style="width: 30px; background: #006380; padding: 13px; border-radius: 20px;"
               src="../assets/hotelServic.svg">
          <div class="hotelInfoTextsWrapper">
            <span class="hotelInfoTitle">Услуги</span>
            <span class="hotelInfoTexts">
              Wifi на всей территории и в номерах
              <br/>
              Ресторан
              <br/>
              Парковка на территории отеля
              <br/>
              Трансфер c Аэропорта до Отеля
              <br/>
              Питание согласно выбранному тарифу
              <br/>
              Бассейн для детей
          </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hotelInfo',
  data() {
    return {
      drawer: false,
      currentDate: new Date(),
    };
  },
};
</script>

<style lang="scss" scoped>
.hotelInfo{
  margin-top: 30px;
}
.hotelInfoWrapper{
  margin-top: 50px;
  border-radius: 12px;
  padding: 20px;
  color: rgba(65, 59, 59, 0.78);
}
.hotelInfoTextsWrapper{
  display: flex;
  flex-flow: column;
}
.hotelInfoTitle{
  font-weight: bold;
  font-size: 23px;
}
.hotelInfoTexts{
  font-weight: 300;
  font-size: 18px;
}
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both
}
</style>
