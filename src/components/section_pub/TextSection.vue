<template>
  <section id="textType" class="text__wrap" :class="attr">
    <span>JEJU sari PICK</span>
    <h2 class="mb70">RECOMMEND</h2>
    <div class="text__inner" :class="layout">
      <div class="text t1">
        <h3 class="text__title">사려니숲길</h3>
        <p class="text__desc">
          비자림로를 시작으로 물찻오름과 사려니 오름을 거쳐가는 삼나무가 우거진
          숲길입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t2">
        <h3 class="text__title">박수기정</h3>
        <p class="text__desc">
          "바가지로 마실 수 있는 깨끗한 샘물이 솟아나는 절벽"이라는 뜻을 가지고
          있는 제주 명소입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t3">
        <h3 class="text__title">휴애리 자연생활공원</h3>
        <p class="text__desc">
          각 계절마다 꽃축제가 열리며 다양한 볼거리를 제공해 주는 핫플레이스
          관광지입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t4">
        <h3 class="text__title">산방산</h3>
        <p class="text__desc">
          서남부의 평야지대에 우뚝 서 있는 곳으로 어디서든 조망할 수 잇는
          아름다운 명소입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t5">
        <h3 class="text__title">카멜리아힐</h3>
        <p class="text__desc">
          동양 최대 규모의 동백 수목원으로 각종 조경수와 함께 어우러진
          수목원입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
      </div>
      <div class="text t6">
        <h3 class="text__title">성읍 민속마을</h3>
        <p class="text__desc">
          옛 마을 형태의 민속 경관이 잘 유지되어 있어 제주도 옛 민가의 특징이 잘
          간직되어 있는 곳입니다.
        </p>
        <a class="text__btn" href="#">더보기</a>
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
/* textType */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #f5f5f5;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text__btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}

@media (max-width: 960px) {
  .text {
    width: 49%;
    background: #f5f5f5;
  }
}
@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}
@media (max-width: 480px) {
  .text {
    width: 100%;
  }
  .text__title {
    text-align: center;
  }
  .text__title::before {
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  .text__desc {
    text-align: center;
  }
  .text__btn {
    text-align: right;
  }
}
</style>
