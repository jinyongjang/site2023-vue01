<template>
  <section
    id="memberSection"
    class="member__wrap gmarket5 section center bg-blue"
  >
    <h3>멤버 소개</h3>
    <p>웹디자이너, 웹 퍼블리셔, 프론트앤드 개발자 멤버를 소개합니다.</p>
    <div class="member__inner container">
      <article class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/peep-1.svg" alt="멤버" />
        </figure>
        <div class="member__body">
          <h4>웹디자이너</h4>
          <p class="desc">김고은(31)</p>
          <a href="/" class="btn"></a>
        </div>
      </article>
      <article class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/peep-2.svg" alt="멤버" />
        </figure>
        <div class="member__body">
          <h4>웹 퍼블리셔</h4>
          <p class="desc">공유(42)</p>
          <a href="/" class="btn"></a>
        </div>
      </article>
      <article class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/peep-3.svg" alt="멤버" />
        </figure>
        <div class="member__body">
          <h4>프론트엔드</h4>
          <p class="desc">이동욱(38)</p>
          <a href="/" class="btn"></a>
        </div>
      </article>
    </div>
  </section>
</template>

<style lang="scss">
//member__wrap

.member__inner {
  @include flex-between;

  .member {
    width: 32%;
    border: 2px solid var(--color_body);

    .member__header {
      margin-top: -20px;

      img {
        object-fit: cover;
        width: 100%;
      }
    }
    .member__body {
      margin-top: -90px;
      padding: 15px 10px;
      background: #000;
      color: #fff;
      z-index: 100;
      position: relative;

      h4 {
        font-size: 22px;
      }

      a {
        color: #fff;
        text-decoration: underline;
        text-underline-position: under;
      }
    }
  }
}
</style>
