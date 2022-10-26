<template>
  <section id="imgTextType" class="imgText__wrap" :class="attr">
    <h2 class="blind">유용한 사이트 살펴보기</h2>
    <div class="imgText__inner container">
      <div class="imgText__txt" :class="layout">
        <span>STAY</span>
        <h3>JEJU sari Interior</h3>
        <p>
          모던하고 아늑한 분위기로 제주 자연의 따뜻함과 청량함을 객실에 그대로
          담았습니다.
        </p>
        <ul>
          <li><a href="#">Deluxe</a></li>
          <li><a href="#">Deluxe Family</a></li>
          <li><a href="#">Premier</a></li>
          <li><a href="#">Premier Family</a></li>
          <li><a href="#">Junior Suite</a></li>
          <li><a href="#">Junior Suite Family</a></li>
        </ul>
      </div>
      <div class="imgText__img img1">
        <a href="#">Deluxe</a>
      </div>
      <div class="imgText__img img2">
        <a href="#">Deluxe Family</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>

<style>
/* imgTextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
}
.imgText__inner > div {
  width: 32%;
  height: 500px;
}
.imgText__txt {
}
.imgText__txt span {
  font-size: 16px;
  color: #999;
  text-decoration: underline;
  text-combine-upright: under;
  margin-bottom: 20px;
  display: block;
}
.imgText__txt h3 {
  font-size: 50px;
  font-weight: 300;
  margin-bottom: 20px;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #999;
  margin-bottom: 10px;
}
.imgText__txt ul {
  font-size: 19px;
  font-weight: 300;
  line-height: 1.6;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #999;
}
.imgText__txt ul li:before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 10px;
  background: #999;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: #27232077;
  color: #fff;
  font-size: 18px;
  padding: 10px 30px;
  border-radius: 30px;
  display: inline-block;
  transition: padding 0.5s;
}
.imgText__img.img1:hover a {
  padding: 10px 120px;
}
.imgText__img.img2:hover a {
  padding: 10px 90px;
}
.imgText__img.img1 {
  background: url(../../assets/img/imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgText_bg02.jpg) no-repeat center / cover;
}

@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 40px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__txt {
    width: 100%;
    height: auto;
    text-align: center;
  }
  .imgText__inner > div.imgText__txt ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 49%;
  }
}
@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 200px;
  }
  .imgText__inner > div.imgText__img.img1 {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
  .imgText__img.img1:hover a {
    padding: 10px 180px;
  }
  .imgText__img.img2:hover a {
    padding: 10px 150px;
  }
}
</style>
