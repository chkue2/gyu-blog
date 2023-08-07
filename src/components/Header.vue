<script>
import { onMounted, ref } from "vue";
export default {
  setup() {
    const isScroll = ref(false);
    const menus = ["About", "Skills", "Projects", "Careers"];
    onMounted(() => {
      handlerScrollEvent();
      window.addEventListener("scroll", () => {
        handlerScrollEvent();
      });
    });

    const handlerScrollEvent = () => {
      isScroll.value = window.scrollY > 30;
    };

    const handlerClickHeaderItem = (text) => {
      switch (text) {
        case "About":
          scrollIntoViewToTarget("#sectionAbout");
          break;
        case "Skills":
          scrollIntoViewToTarget("#sectionSkills");
          break;
        case "Projects":
          scrollIntoViewToTarget("#sectionProjects");
          break;
        case "Careers":
          scrollIntoViewToTarget("#sectionCareers");
          break;
        default:
          return;
      }
    };

    const scrollIntoViewToTarget = (target) => {
      const scrollPosition =
        document.querySelector(target).offsetTop -
        document.querySelector(".header-wrapper").clientHeight;

      window.scrollTo({ top: scrollPosition, behavior: "smooth" });
    };

    return {
      isScroll,
      menus,
      handlerClickHeaderItem,
    };
  },
};
</script>
<template>
  <header :class="{ scrolling: isScroll === true }">
    <div class="header-wrapper">
      <a
        v-for="(menu, index) in menus"
        :key="index"
        class="header-item"
        @click="handlerClickHeaderItem(menu)"
        >{{ menu }}</a
      >
    </div>
  </header>
</template>
<style scoped lang="scss">
header {
  position: fixed;
  top: 0;
  width: 100vw;
  transition: background-color 0.3s ease-in-out;
  &.scrolling {
    background-color: rgba(0, 0, 0, 0.8);
  }
  .header-wrapper {
    max-width: 1024px;
    width: 100%;
    margin: 0 auto;
    height: 80px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    gap: 24px;
    padding: 0 24px;
    box-sizing: border-box;
  }
  .header-item {
    font-size: 18px;
    cursor: pointer;
    color: #ffffff;
    transition: color 0.3s ease-in-out;
    &:hover {
      opacity: 0.8;
    }
  }
}
@media all and (max-width: 500px) {
  header {
    .header-wrapper {
      height: 60px;
    }
    .header-item {
      font-size: 14px;
    }
  }
}
</style>
