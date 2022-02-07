<template>
  <div class="header">
    <div class="headerWrapper">
      <img class="logoImg" src="../assets/logotype.png" />
      <div class="locationText">
        <span>
          <img class="locationImg" src="../assets/locationImg.png">
          Республика Дагестан
          <br />
          Карабудахкентский район.
          <br />
          п.Манас
        </span>
      </div>
      <div v-if="width > 800" class="contactsWrapper">
        <a class="contactIcon" href="tel:+79285021444" data-v-8068cd08="">
          <img class="contactIconImg" src="../assets/phone.svg">
        </a>
<!--          <a class="tel" href=”tel:+79285021444”><img src="../assets/phone.svg"></a>-->
        <a class="contactIcon" href="https://www.instagram.com/hotel_prichal/" target="_blank">
          <img class="contactIconImg" src="../assets/icons8-instagram.svg">
        </a>
        <a class="contactIcon" href="https://wa.me/79285021444" target="_blank">
          <img class="contactIconImg" src="../assets/whatsapp.svg">
        </a>
        <a class="contactIcon" href="https://telegram.me/hvlyk" target="_blank">
          <img class="contactIconImg" src="../assets/telegram.svg">
        </a>
      </div>
      <div v-else>
        <img @click="drawer = true"
             src="../assets/burgerMenu.svg"
             style="fill: white; width: 25px"
        />
        <el-drawer
          title="I am the title"
          :visible.sync="drawer"
          :with-header="false"
        >
          <div class="contactsWrapperDrawer">
            <a class="contactIcon" href="tel:+79285021444" data-v-8068cd08="">
              <img class="contactIconImg" src="../assets/phone.svg">
            </a>
            <a class="contactIcon" href="https://www.instagram.com/hotel_prichal/" target="_blank">
              <img class="contactIconImg" src="../assets/icons8-instagram.svg">
            </a>
            <a class="contactIcon" href="https://wa.me/79285021444" target="_blank">
              <img class="contactIconImg" src="../assets/whatsapp.svg">
            </a>
            <a class="contactIcon" href="https://telegram.me/hvlyk" target="_blank">
              <img class="contactIconImg" src="../assets/telegram.svg">
            </a>
          </div>
        </el-drawer>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'header',
  data() {
    return {
      drawer: false,
      width: 0,
    };
  },
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
    },
  },
  created() {
    window.addEventListener('resize', this.updateWidth);
    this.updateWidth();
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url("https://fonts.googleapis.com");
@import url("https://fonts.gstatic.com");
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600&display=swap");

.header {
  display: flex;
  justify-content: center;
  position: absolute;
  color: white;
  z-index: 3000;
  width: 100%;
  font-family: Montserrat;
}
.logoImg {
  width: 220px;
}
.headerWrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 0 20px 0 20px;
}

.tel{
  color: white;
  font-size: 25px;
}
.locationText{
  display: flex;
  margin: 0 20px;
  //width: 150px;
}
@media (max-width: 600px) {
  //.locationText{
  //  margin-bottom: 30px;
  //}
}
.contactsWrapper{
  display: flex;
  align-items: baseline;
}
.contactsWrapperDrawer{
  display: flex;
  align-items: center;
  flex-flow: column;
  margin-top: 20px;
}
.contactIcon{
  margin-right: 20px;
}
.locationImg{
  width: 20px;
}
@media screen and (max-width: 800px) {
  .headerWrapper{
    margin-top: 10px;
    align-items: center;
    padding: 0 10px 0 10px;
  }
  .tel{
    font-size: 10px;
  }
  .locationText{
    font-size: 10px;
  }
  .logoImg{
    width: 100px;
  }
  .locationImg{
    width: 10px;
  }
  .contactIconImg{
    width: 20px;
  }
  .contactIcon{
    margin-top: 10px;
    margin-right: 10px;
  }
  .contactsWrapper{
    flex-flow: column;
  }
}
</style>
