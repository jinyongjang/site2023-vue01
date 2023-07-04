<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">프론트앤드 커리큘럼 과정 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>Web Publisher</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 :class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>
            {{ text.desc }}
          </p>
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
      title: "웹퍼블리셔<br />전문과정",
      desc: "프론트엔드 개발자로 취업하기 위한<br />전문 과정입니다",
      texts: [
        {
          title: "웹 디자인",
          desc: "웹디자인은 웹사이트를 만들기 위해 시각적인 요소와 사용자 경험을 디자인하는 과정을 말합니다. 웹디자인은 웹사이트의 레이아웃, 색상, 그래픽, 폰트, 이미지 등을 결정하는 작업을 포함합니다. 이를 통해 사용자가 웹사이트를 방문했을 때 시각적으로 매력적이고 사용하기 쉽도록 만들어줍니다.",
        },
        {
          title: "웹 퍼블리셔",
          desc: "웹 퍼블리셔는 디자이너나 개발자가 제공한 디자인 파일이나프로토타입을 기반으로 웹페이지를 만들고 공개하는 역할을수행합니다. 웹 퍼블리셔는 HTML, CSS, JavaScript 등의 웹 기술을사용하여 디자인을 웹사이트로 구현하고, 브라우저에서 올바르게 작동하도록 합니다.",
        },
        {
          title: "React.js",
          desc: "React.js는 사용자 인터페이스(UI)를 구축하기 위한 JavaScript 라이브러리입니다. 페이스북에서 개발하였으며, 단일 페이지 애플리케이션(SPAs) 및 대규모 애플리케이션 개발에 주로 사용됩니다.",
        },
        {
          title: "Vue.js",
          desc: "Vue.js는 사용자 인터페이스(UI)를 구축하기 위한 프로그레시브 프레임워크입니다. Vue.js는 사용자 인터페이스를 개발하기 위한 JavaScript 프레임워크로, 가볍고 유연한 구조를 가지고 있으며, 단일 페이지 애플리케이션(SPAs) 및 웹 애플리케이션의 개발에 주로 사용됩니다.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
// intro__wrap

.intro__inner {
  font-family: "NexonLv1Gothic";
  display: flex;
  justify-content: space-between;
}
.intro__title {
  width: 33%;

  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 30px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  > div {
    width: 48%;
    margin-bottom: 40px;

    h4 {
      font-size: 24px;
      margin-bottom: 15px;
    }
    &:nth-child(3) {
      margin-bottom: 0;
    }
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
