<script>
export default {
  setup() {
    const infoData = [
      {
        class: "fa-solid fa-user",
        title: "이름",
        content: "최한규",
      },
      {
        class: "fa-solid fa-calendar",
        title: "생년월일",
        content: "1993.11.16",
      },
      {
        class: "fa-solid fa-location-dot",
        title: "주소지",
        content: "경기도 안산시 단원구",
      },
      {
        class: "fa-solid fa-phone",
        title: "연락처",
        content: "010-4422-9393",
        isPhone: true,
      },
      {
        class: "fa-solid fa-envelope",
        title: "이메일",
        content: "chkue0924@kakao.com",
        isEmail: true,
      },
      {
        class: "fa-solid fa-school",
        title: "최종학력",
        content: "학점은행제(학사)",
      },
    ];

    return {
      infoData,
    };
  },
};
</script>
<template>
  <div id="sectionAbout" class="section-about">
    <div class="section-middle section-max-width section-padding">
      <h2 class="section-title">ABOUT</h2>
      <div class="section-about-grid">
        <div
          v-for="(info, index) in infoData"
          :key="index"
          class="section-about-grid-item"
        >
          <i :class="info.class"></i>
          <div class="section-about-grid-item-right">
            <p class="section-about-grid-item-title">{{ info.title }}</p>
            <a
              v-if="info.isPhone === true"
              class="section-about-grid-item-content"
              :href="`tel:${info.content}`"
              >{{ info.content }}</a
            >
            <a
              v-else-if="info.isEmail === true"
              class="section-about-grid-item-content"
              :href="`mailto:${info.content}`"
              >{{ info.content }}</a
            >
            <p v-else class="section-about-grid-item-content">
              {{ info.content }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
.section-about {
  padding: 60px 0;
  .section-about-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 48px;
  }
  .section-about-grid-item {
    display: flex;
    align-items: center;
    gap: 24px;
    & > i {
      font-size: 35px;
      min-width: 45px;
      text-align: center;
    }
  }
  .section-about-grid-item-title {
    font-size: 20px;
    font-weight: 500;
  }
  .section-about-grid-item-content {
    font-size: 24px;
    font-weight: 600;
    color: #000000;
  }
}
@media all and (max-width: 1024px) {
  .section-about {
    .section-about-grid {
      grid-template-columns: repeat(2, 1fr);
      grid-gap: 24px;
    }
    .section-about-grid-item {
      display: flex;
      align-items: center;
      gap: 12px;
      & > i {
        font-size: 20px;
        min-width: 20px;
        text-align: center;
      }
    }
    .section-about-grid-item-title {
      font-size: 16px;
      font-weight: 500;
    }
    .section-about-grid-item-content {
      font-size: 18px;
      font-weight: 600;
      color: #000000;
    }
  }
}
@media all and (max-width: 500px) {
  .section-about {
    padding: 40px 0;
    .section-about-grid-item-title {
      font-size: 12px;
      font-weight: 500;
    }
    .section-about-grid-item-content {
      font-size: 12px;
      font-weight: 600;
      color: #000000;
    }
  }
}
</style>
