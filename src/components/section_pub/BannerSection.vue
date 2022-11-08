<template>
  <section id="bannerType" class="banner__wrap" :class="attr">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="banner__title">RESERVATION</h3>
      <p class="banner__desc">
        아래 링크를 통해 실시간 예약 일정을 확인하실 수 있습니다.
        <a href="#" title="새페이지 열림">reservation.com/c/JEJUsari</a>
      </p>
      <span class="banner__small">JEJU sari</span>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
};
</script>

<style>
.banner__inner {
  background-image: url(../../assets/img/banner_bg01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
  opacity: 0.95;
}
.banner__title {
  font-size: 50px;
  line-height: 1;
  font-weight: 300;
  margin-bottom: 40px;
}
.banner__desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__desc span {
  display: none;
  font-size: 24px;
  font-weight: 300;
}
.banner__desc a {
  color: #fff;
  display: block;
}
.banner__desc a:hover {
  text-decoration: underline;
  color: #000;
}
.banner__small {
  font-size: 16px;
  text-decoration: underline;
}

@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
