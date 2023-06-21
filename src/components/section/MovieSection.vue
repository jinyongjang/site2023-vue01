<template>
  <section id="moviesSection" :class="attr">
    <div class="movie__inner">
      <div class="movie__inner container">
        <div class="movie__text">
          <h3>코딩 추천 영화</h3>
          <p>
            Netflix와 Youtube등 다양한 경로에서
            <br />
            코딩 관련 영화를 시청할 수 있습니다.
          </p>
          <a href="/" class="button-green"> 자세히 보기 </a>
        </div>
        <div class="movie__item">
          <div>
            <img src="@/assets/images/movie/movieImg.png" alt="영화" />
          </div>
          <div>
            <img src="@/assets/images/movie/movieImg02.png" alt="영화" />
          </div>
          <div>
            <img src="@/assets/images/movie/movieImg03.png" alt="영화" />
          </div>
          <div>
            <img src="@/assets/images/movie/movieImg04.png" alt="영화" />
          </div>
          <div>
            <img src="@/assets/images/movie/movieImg04.png" alt="영화" />
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
};
</script>

<style lang="scss">
.movie__wrap {
  overflow: hidden;
}
.movie__inner {
  height: 1000px;
  margin-top: 100px;
  margin-bottom: 100px;
  .movie__text {
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

  .movie__item {
    @include flex-between;
    position: absolute;
    margin-top: 70px;

    > div {
      margin-right: 10px;
      width: 400px;
      @include border(20px);
    }
    > div img {
      width: 100%;
    }
  }
}

.movie__tag {
  ul {
    font-family: "GmarketSans";
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

//movie__search
.movie__search {
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
    @include button(#ff0000, #fff);
    border-radius: 50px;
    font-family: "GmarketSans";
  }
}

//movie__page
.movie__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    font-family: "GmarketSans";

    li {
      width: 24.3%;
      position: relative;
      margin-bottom: 2%;

      .title {
        font-size: 20px;
        padding: 3px 0;
        display: inline-block;

        &:hover {
          text-decoration: underline;
          text-underline-position: under;
        }
      }
      .star {
        position: absolute;
        right: 20px;
        top: 20px;
        height: 30px;
        width: 30px;
        text-align: center;
        background-color: #fff;
        line-height: 30px;
        border-radius: 50%;
        font-size: 12px;
      }
    }
  }
}
</style>
