<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="unsplash__text">
        <h3>Unsplash</h3>
        <p>
          Unsplash에서 다양한 이미지를 무료로
          <br />
          사용할 수 있습니다.
        </p>
        <a href="/" class="button-blue"> 자세히 보기 </a>
      </div>
      <div class="unsplash__item">
        <div>
          <img
            src="@/assets/images/unsplash/unsplashImg.png"
            alt="언스플래쉬"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplashImg02.png"
            alt="언스플래쉬"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplashImg03.png"
            alt="언스플래쉬"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplashImg04.png"
            alt="언스플래쉬"
          />
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
};
</script>

<style lang="scss">
.unsplash__wrap {
  overflow: hidden;
}
.unsplash__inner {
  height: 600px;

  .unsplash__text {
    h3 {
      font-size: 50px;
      margin-bottom: 40px;
    }
    p {
      font-size: 22px;
      font-weight: 300;
      margin-bottom: 60px;
    }
    a {
      @include border(50px);
    }
  }

  .unsplash__item {
    @include flex-between;
    margin-top: 70px;
    position: absolute;

    > div {
      width: 400px;
      margin-right: 10px;
    }
    > div img {
      width: 100%;
      @include border(20px);
    }
  }
}

//unsplash__page
.unsplash__cont {
  ul {
    column-count: 4;
    column-gap: 20px;
    li {
      margin-bottom: 20px;
    }
  }
}

//unsplash__search
.unsplash__search {
  text-align: center;
  margin-bottom: 50px;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    border-radius: 50px;
    min-width: 300px;
    margin-right: 10px;
    font-family: "GmarketSans";
  }
  button {
    @include button(#4857ec, #fff);
    border-radius: 50px;
    font-family: "GmarketSans";
  }
}
</style>
