<template>
  <div class="section-top">
    <div class="section-middle section-max-width section-padding">
      <h1>최한규<br />프론트엔드 개발자 포트폴리오</h1>
      <p class="section-top-intro">
        안녕하세요👋 사용자 경험을 높여주는 개발자 최한규입니다.<br />
        협업을 위해 배려하며, 배움을 두려워하지 않습니다.
      </p>
    </div>
  </div>
</template>
<style scoped lang="scss">
.section-top {
  width: 100vw;
  background: url("../assets/images/section-top-2.jpg") no-repeat center/cover;
  h1 {
    margin: 0;
    text-align: center;
    padding-top: calc(60px + 80px);
    color: #ffffff;
    font-size: 48px;
    line-height: 1.3;
  }
  .section-top-intro {
    text-align: center;
    padding-bottom: 60px;
    font-size: 20px;
    font-weight: 500;
    color: #f5f5f5;
    text-shadow: 0px 0px 5px #000000;
    margin: 0;
    margin-top: 24px;
  }
}
@media all and (max-width: 1024px) {
  .section-top {
    h1 {
      font-size: 36px;
    }
    .section-top-intro {
      font-size: 18px;
    }
  }
}
@media all and (max-width: 500px) {
  .section-top {
    h1 {
      font-size: 26px;
    }
    .section-top-intro {
      font-size: 14px;
    }
  }
}
</style>
