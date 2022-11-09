<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>{{ cardTypes[0].h2 }}</h2>
    <p>{{ cardTypes[0].p }}</p>
    <div class="card__inner" :class="layout">
      <article class="card" v-for="card in cards" v-bind:key="card.cards">
        <figure class="card__header">
          <img :src="card.img" :alt="card.tit" />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{ card.tit }}</h3>
          <p class="desc">{{ card.desc }}</p>
          <a href="#">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0L0 4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
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
  data: function () {
    return {
      cardTypes: [
        {
          h2: "FACILITIES",
          p: "새로운 경험을 배울 수 있는 공간에서 진정한 휴식을 만끽하시길 바랍니다.",
        },
      ],
      cards: [
        {
          img: "https://github.com/kkb75281/vueclass/blob/main/src/assets/img/card_bg01_01.jpg?raw=true",
          tit: "Family Lounge",
          desc: "가족과 함께하는 여행, 편안한 휴식을 선사하고자 합니다. 패밀리 라운지는 오션뷰가 아름다운 라운지 공간과 컬러풀한 디자인으로 마련된 어린이 클래스 공간으로 나눠져 있습니다.",
        },
        {
          img: "https://github.com/kkb75281/vueclass/blob/main/src/assets/img/card_bg01_02.jpg?raw=true",
          tit: "Outdoor Pool",
          desc: "제주 바다의 푸르름, 파도소리와 어우러지는 음악은 여정을 더욱 즐겁게 만듭니다. 청정한 공기로 가득한 휴식공간에서 자쿠지의 따뜻함에 기대 푸른 별을 바라보면, 휴식의 진정한 본질을 깨달을 수 있습니다.",
        },
        {
          img: "https://github.com/kkb75281/vueclass/blob/main/src/assets/img/card_bg01_03.jpg?raw=true",
          tit: "Meeting Room",
          desc: "프라이빗하고 고급스러운 분위기의 미팅룸으로 임원 미팅 및 VIP 행사에 적합합니다. 소그룹부터 대그룹의 인원까지 수용가능한 미팅룸으로",
        },
      ],
    };
  },
};
</script>

<style>
/* cardType */
.card__inner {
  display: flex;
  justify-content: space-between;
  position: relative; /* 정렬 맞게 배치 */
}
.card {
  width: 32%;
  background-color: #f5f5f5;
  overflow: hidden;
  transition: all 0.3s;
}
.card:hover {
  box-shadow: 4px 4px 5px 0 rgba(0, 0, 0, 0.2);
}
.card:hover .card__header {
  scale: 1.03;
}
.card__header {
  height: 450px;
  overflow: hidden;
  transform-origin: bottom center;
  transition: all 0.3s;
}
.card__body {
  padding: 24px;
}
.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  /* 한줄효과 */
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  padding-right: 20px;
}
.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  /* 세줄효과 */
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}

@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
  }
}
</style>
