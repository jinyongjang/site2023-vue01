<template>
  <section id="youtubeSection" :class="attr">
    <div class="youtube__inner container">
      <div class="youtube__text">
        <h3>코딩 유튜버 추천</h3>
        <p>
          노마드 코더, 애플 코딩 등 많은 유튜버들이 있습니다. <br />
          함께 공부 합시다.
        </p>
        <a href="/" class="button-red"> 자세히 보기 </a>
      </div>
      <div class="youtube__item">
        <div>
          <img src="@/assets/images/youtube/youtubeImg.png" alt="유튜브" />
        </div>
        <div>
          <img src="@/assets/images/youtube/youtubeImg02.png" alt="유튜브" />
        </div>
        <div>
          <img src="@/assets/images/youtube/youtubeImg03.png" alt="유튜브" />
        </div>
        <div>
          <img src="@/assets/images/youtube/youtubeImg04.png" alt="유튜브" />
        </div>
        <div>
          <img src="@/assets/images/youtube/youtubeImg05.png" alt="유튜브" />
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
//youtube__section
.youtube__wrap {
  overflow: hidden;
}
.youtube__inner {
  height: 600px;
  .youtube__text {
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

  .youtube__item {
    @include flex-between;
    position: absolute;
    margin-top: 70px;

    > div {
      margin-right: 10px;
      width: 400px;
      @include border(20px);
    }
  }
}

// youtube__page
.youtube__slider {
  display: none;
}
.youtube__search {
  margin-bottom: 50px;
  text-align: center;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
    font-family: "GmarketSans";
  }
  button {
    @include button(#f7100d, #ffffff);
    @include border(50px);
    font-family: "GmarketSans";
  }
}
.youtube__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    margin-top: 100px;

    li {
      a {
        border: 1px solid #f52323;
        padding: 10px 20px;
        margin: 0 10px;
        color: #f7100d;
      }
    }
  }
}

.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 31.333%;
      margin-bottom: 4%;

      span {
        display: block;
        margin: 4px 0;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        -webkit-line-clamp: 1; /* 라인수 */
        -webkit-box-orient: vertical;
        word-wrap: break-word;
      }

      img {
        width: 100%;
      }
    }
  }
}
</style>
