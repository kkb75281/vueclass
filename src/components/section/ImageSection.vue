<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>Premier</h2>
    <p>
      넓은 잔디가 있는 마당과 편안한 휴식을 즐길 수 있는 야외 수영장이 즐거움을
      줍니다.
    </p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title"><em>with</em> GARDEN</h3>
        <p class="image__desc">
          어느 객실에서나 광활한 원시림을 마주합니다. 숲에 안겨 있는
          레스트리처럼 몸과 마음을 맡긴채 온전한 자유를 누려보세요.
        </p>
        <a class="image__btn" href="#" title="자세히 보기">more ></a>
      </article>
      <article class="image img2">
        <h3 class="image__title"><em>with</em> POOL</h3>
        <p class="image__desc">
          탁트인 풍경과 함께하는 독채수영장은 남녀노소 편안한 휴식과 즐거움을
          극대화하는 JEJU sari 만의 특색입니다.
        </p>
        <a class="image__btn gray" href="#" title="자세히 보기">more ></a>
      </article>
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
/* imageType */
.image__inner {
  display: flex;
  /* flex-wrap: wrap; */
  justify-content: space-between;
}
.image {
  width: 49%;
  height: 370px;
  color: #fff;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
  position: relative;
  transition: scale 0.3s;
}
.image.img1 {
  background: url(../../assets/img/image_bg01_01.jpg) no-repeat center;
  /* opacity: 0.9; */
}
.image.img2 {
  background: url(../../assets/img/image_bg01_02.jpg) no-repeat center;
  /* opacity: 0.9; */
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  padding-top: 50px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__title em {
  font-style: normal;
  font-size: 22px;
  font-weight: 300;
}
.image__desc {
  font-size: 16px;
  font-weight: 300;
  margin-bottom: 10px;
  line-height: 1.5;
  /* 세줄효과 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.image__btn {
  display: none;
  text-align: center;
  font-size: 16px;
  background-color: rgba(0, 0, 0, 0.4);
  color: #fff;
  width: 100%;
  padding: 175px 0;
  position: absolute;
  content: "";
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.image:hover .image__btn {
  display: block;
}
.image:hover {
  scale: 0.98;
}

@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 210px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
  .image__desc {
    font-size: 16px;
  }
}
</style>
