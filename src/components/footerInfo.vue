<template>
  <div class="footer-info-container">
    <div class="footer-info-text-wrapper">
      <div class="hotel-logo-info">
        <span class="footer-text">👇 Как нас найти 👇</span>
      </div>
    </div>
    <div style="position:relative;overflow:hidden; width: 100%">
      <a
        href="https://yandex.ru/maps/org/dom_otdykha_prichal/143106843798/?utm_medium=mapframe&utm_source=maps"
        style="color:#eee;font-size:12px;position:absolute;top:0px;">Дом отдыха Причал</a>
      <a
        href="https://yandex.ru/maps/11010/republic-of-dagestan/category/hotel/184106414/?utm_medium=mapframe&utm_source=maps"
        style="color:#eee;font-size:12px;position:absolute;top:14px;">
        Гостиница в Республике Дагестан
      </a>
      <iframe
        src="https://yandex.ru/map-widget/v1/-/CCU5mKFYXB" height="500" frameborder="1"
        allowfullscreen="true"
        style="position:relative; width: 100%; border: none"
      >
      </iframe>
    </div>
  </div>
</template>

<script>
export default {
  name: 'footerInfo',
};
</script>

<style lang="scss" scoped>
.footer-info-container{
  margin-top: 30px;
  .footer-info-text-wrapper{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
    .hotel-logo-info{
      display: flex;
      align-items: center;
      flex-flow: column;
    }
    .footer-text {
      font-family: Montserrat;
      font-size: 25px;
    }
  }
  .logo{
    width: 300px;
  }
}
</style>
