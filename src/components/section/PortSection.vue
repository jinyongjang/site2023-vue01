<template>
  <section id="portSection" :class="attr">
    <h3>쉬어가기 꽃 소개</h3>
    <p>
      꽃은 아름다움과 향기로운 특징을 지니며, 심신 안정과 안락함을 전해주는
      자연의 아름다운 선물입니다.
    </p>
    <div class="port__inner container">
      <div class="port__btn">
        <ul>
          <li>
            <a href="/">봄</a>
          </li>
          <li>
            <a href="/">여름</a>
          </li>
          <li>
            <a href="/">가을</a>
          </li>
          <li>
            <a href="/">겨울</a>
          </li>
        </ul>
      </div>
      <div class="port__cont">
        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="port__header">
            <img :src="text.img" :alt="text.title" />
          </figure>
          <div class="port__body">
            <div class="pic">
              <img :src="text.icon" :alt="text.title" />
            </div>
            <div>
              <h4>{{ text.title }}</h4>
              <p>
                {{ text.desc }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      texts: [
        {
          img: "./images/port/portImg01.svg",
          title: "국화",
          desc: "우아하고 아름다운 꽃으로,전통적인 아시아 문화에서 미를 상징",
          icon: "./images/port/memberIcon01.png",
        },
        {
          img: "./images/port/portImg02.svg",
          title: "데이지",
          desc: "신선하고 밝은 느낌을 주는 꽃으로,순수함과 희망을 상징",
          icon: "./images/port/memberIcon01.png",
        },
        {
          img: "./images/port/portImg03.svg",
          title: "장미",
          desc: "사랑과 열정을 상징하는 아름다운 꽃으로,그 향기와 우아함으로 인기있는 꽃",
          icon: "./images/port/memberIcon01.png",
        },
        {
          img: "./images/port/portImg04.svg",
          title: "제비꽃",
          desc: "자유로움과 희망을 상징하는 아름다운 꽃",
          icon: "./images/port/memberIcon01.png",
        },
        {
          img: "./images/port/portImg05.svg",
          title: "아이리스",
          desc: "꽃잎과 섬세한 모양으로 유명한 꽃으로,우아함과 지혜를 상징하는 꽃",
          icon: "./images/port/memberIcon01.png",
        },
        {
          img: "./images/port/portImg06.svg",
          title: "벚꽃",
          desc: "아름다운 분홍빛 꽃을 피우며,잠시동안만 지속되는 아름다운 순간을 상징하는 꽃",
          icon: "./images/port/memberIcon01.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
//port__wrap
.port__wrap {
  font-family: "Ansungtangmyun";
}
.port__inner {
  .port__btn {
    ul {
      display: flex;
      justify-content: center;
      margin-bottom: 50px;
      li {
        margin-right: 10px;
        a {
          border: 1px solid #000;
          display: inline-block;
          padding: 5px 20px;
          border-radius: 40px;
        }
      }
    }
  }

  .port__cont {
    display: flex;
    flex-wrap: wrap;

    .port {
      width: 33.333%;

      .port__header {
        margin-right: 30px;
      }

      .port__body {
        display: flex;
        align-items: center;
        margin: 30px 30px 30px 0;
      }
      .pic {
        margin-right: 20px;
      }

      img {
        width: 100%;
      }
      h4 {
        text-align: left;
        font-size: 20px;
        font-weight: bold;
      }
      p {
        text-align: left;
      }
    }
  }
}
</style>
