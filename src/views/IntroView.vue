<template>
  <main>
    <div className="intro__wrap container gmarket section">
      <div className="introcard1">
        <div className="introImg"></div>
        <div className="introDesc">
          <h1>About</h1>
          <p>
            Vue.js는 사용자 인터페이스를 구축하기 위한 progressiven JavaScript
            프레임워크입니다. Vue.js는 웹 애플리케이션 개발을 위해 사용되며,
            단일 페이지 애플리케이션(Single-Page Application, SPA) 및 복잡한
            사용자 인터페이스를 구축하는 데 적합합니다. Vue.js는 가볍고 유연한
            구조를 가지고 있으며, HTML, CSS 및 JavaScript와의 간편한 통합을
            제공합니다. Vue.js는 반응성이 있는 데이터 바인딩과 컴포넌트 기반
            아키텍처를 중심으로 구축되어 있습니다. Vue.js의 핵심 기능 중 하나는
            "반응성"입니다. 데이터 모델과 뷰를 연결하여 데이터가 변경될 때
            자동으로 뷰가 업데이트됩니다. 이를 통해 개발자는 직접 DOM 조작이나
            수동 업데이트 로직을 작성할 필요 없이 데이터 상태에 집중할 수
            있습니다.
          </p>
        </div>
      </div>
      <div className="introCard2">
        <h1>History</h1>
        <p>
          Vue.js의 역사는 2013년에 시작되었습니다. 에반 유(Evan You)라는
          개발자가 AngularJS 프레임워크의 몇 가지 제한 사항을 해결하고자 시작한
          개인 프로젝트로 출발했습니다. 에반 유는 AngularJS를 사용하면서
          유연성과 성능 측면에서 일부 제약을 느꼈습니다. 그래서 더 가벼운
          프레임워크가 필요하다는 아이디어를 갖게 되었고, 이를 기반으로 Vue.js를
          개발하기 시작했습니다.<br />
          2014년 2월, 에반 유는 처음으로 Vue.js를 공개하였고, 초기 버전인
          0.6.0이 릴리스되었습니다. Vue.js는 빠른 성장을 거듭하면서 커뮤니티의
          관심을 받게 되었고, 다양한 기능과 개선사항이 추가되었습니다. 2015년
          10월, Vue.js의 첫 번째 안정 버전인 1.0이 출시되었습니다. 이 버전은
          가상 돔(Virtual DOM) 기반의 리액티브 데이터 바인딩 시스템을 도입하고,
          컴포넌트 기반 아키텍처를 강조했습니다. 이후 Vue.js는 지속적인
          업데이트와 개선을 거쳐 성장하였습니다.<br />
          2016년에는 Vue.js 2.0이 출시되었습니다. 이 버전은 가상 돔(Virtual DOM)
          엔진을 완전히 재작성하여 성능을 향상시키고, 기능적인 면에서도 많은
          개선을 이루었습니다. Vue.js는 점차적으로 인기를 얻어가면서 개발자
          커뮤니티와 기업들의 관심을 받게 되었습니다. Vue.js를 사용하는 기업은
          점점 늘어나고, 커뮤니티에서는 다양한 확장 기능, 플러그인, 컴포넌트
          라이브러리 등이 개발되었습니다.<br />
          2020년 9월에는 Vue.js의 최신 메이저 버전인 Vue 3가 출시되었습니다. Vue
          3는 가상 돔(Virtual DOM) 엔진을 새롭게 개발한 "Vue Router"와 "Vuex"와
          같은 공식 지원 패키지와 함께 제공되며, 성능 개선과 더 나은 개발 경험을
          제공하기 위한 여러 기능과 개선사항이 포함되어 있습니다.
        </p>
      </div>
      <div className="introcard3">
        <h1>Functions</h1>
        <p>
          선언적 렌더링(Declarative Rendering): Vue.js는 템플릿 문법을 사용하여
          데이터를 DOM에 선언적으로 렌더링할 수 있습니다. 이를 통해 개발자는
          직접 DOM 조작을 하지 않고도 데이터의 상태에 따라 자동으로 뷰를
          업데이트할 수 있습니다.<br />
          조건부 렌더링(Conditional Rendering): Vue.js는 v-if나 v-show와 같은
          디렉티브를 제공하여 특정 조건에 따라 요소를 렌더링하거나 숨길 수
          있습니다. <br />
          리스트 렌더링(List Rendering): Vue.js는 v-for 디렉티브를 사용하여 배열
          또는 객체의 각 항목을 기반으로 반복적인 요소를 렌더링할 수 있습니다.
          이벤트 핸들링(Event Handling): Vue.js는 v-on 디렉티브를 사용하여 DOM
          이벤트를 처리할 수 있습니다. 이를 통해 사용자의 액션에 반응하고,
          메서드를 호출하거나 상태를 변경할 수 있습니다.<br />
          컴포넌트 기반 아키텍처(Component-based Architecture): Vue.js는
          컴포넌트를 정의하고 재사용할 수 있는 단위로 구성할 수 있습니다. 이를
          통해 애플리케이션을 구조화하고 유지 보수하기 쉽게 만듭니다.
        </p>
      </div>
    </div>
  </main>
</template>

<style lang="scss">
// intro__wrap
.swiper-scrollbar.swiper-scrollbar-horizontal {
  display: none;
}
.intro__wrap {
}
.intro__inner {
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

.intro__wrap {
  padding-top: 50px;
  .introcard1 {
    display: flex;

    .introImg {
      background-image: url(../assets/images/intro/intro1.png);
      background-size: cover;
      background-position: center center;
      width: 40%;
      height: 550px;
    }
    .introDesc {
      width: 55%;

      h1 {
        color: gold;
        font-weight: bold;
        font-size: 70px;
      }
      p {
        color: #7f5b00;
        padding-left: 20px;
        line-height: 1.6;
        padding-top: 60px;
      }
    }
  }
  .introCard2 {
    padding-top: 50px;
    h1 {
      font-weight: bold;
      font-size: 70px;
      color: salmon;
    }
    p {
      color: #920046;
      font-size: 17px;
      line-height: 1.6;
      padding-left: 20px;
      padding-top: 50px;
    }
  }
  .introcard3 {
    padding-top: 80px;
    h1 {
      font-weight: bold;
      font-size: 70px;
      color: violet;
      text-align: right;
    }
    p {
      color: rgb(160, 59, 160);
      font-size: 17px;
      line-height: 1.6;
      padding-left: 20px;
      padding-top: 50px;
    }
  }
}
</style>
