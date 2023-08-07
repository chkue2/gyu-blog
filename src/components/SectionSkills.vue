<script>
import { computed } from "vue";
export default {
  setup() {
    const skills = {
      frontend: [
        "HTML5",
        "CSS",
        "Javascript",
        "Typescript",
        "Vue.js",
        "Vuex",
        "Nuxt.js",
        "SCSS",
        "jQuery",
        "Metronic",
      ],
      backend: ["Java", "Python", "Firebase", "HeidiSQL", "Oracle"],
      mobileApp: ["Cordova", "Firebase"],
      deployment: ["AWS", "Vite", "Webpack", "Docker", "Tomcat", "Cordova"],
      versionControl: ["Git", "SVN"],
      communication: [
        "Postman",
        "Swagger UI",
        "Notion",
        "Slack",
        "Zeplin",
        "Adobe XD",
      ],
      certificate: ["정보처리산업기사", "네트워크관리사 2급"],
      useLibrary: [
        "moment",
        "lodash",
        "chart.js",
        "Anime.js",
        "AOS",
        "ScrollMagic",
        "gsap",
        "TweenMax",
        "axios",
        "vuetify",
        "vue-cool-lightbox",
        "vue-range-component",
        "vue-slick-carousel",
        "vue-scroll-picker",
        "vue-masonry-css",
      ],
    };

    const tagBackgroundEnum = [
      "#cbff8c",
      "#fff08c",
      "#8cffda",
      "#8ce8ff",
      "#8cffff",
      "#8cd8ff",
      "#ccb0fc",
      "#f0b0fc",
      "#fcb0c8",
      "#fcb0b0",
      "#fcd1b0",
      "#fceeb0",
    ];

    return {
      skills,
      tagBackgroundEnum,
    };
  },
};
</script>
<template>
  <div id="sectionSkills" class="section-skills">
    <div class="section-middle section-max-width section-padding">
      <h2 class="section-title">SKILLS</h2>
      <div class="section-skills-wrapper">
        <div class="section-skills-row">
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">Frontend</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.frontend"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">UseLibrary</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.useLibrary"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
        </div>
        <div class="section-skills-row">
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">Backend</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.backend"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">MobileApp</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.mobileApp"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">Deployment</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.deployment"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">VersionControl</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.versionControl"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
        </div>
        <div class="section-skills-row">
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">Communication</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.communication"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
          <div class="section-skills-row-box">
            <p class="section-skills-row-title">Certificate</p>
            <div class="section-skills-row-tags">
              <span
                v-for="s in skills.certificate"
                :key="s"
                class="section-skills-row-tag"
                :style="{
                  backgroundColor:
                    tagBackgroundEnum[
                      Math.floor(Math.random() * tagBackgroundEnum.length)
                    ],
                }"
              >
                {{ s }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
.section-skills {
  padding: 60px 0;
  background-color: #f5f5f5;
}
.section-skills-wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 24px;
}
.section-skills-row {
  display: flex;
  flex-direction: column;
  gap: 24px;
}
.section-skills-row-box {
  display: flex;
  flex-direction: column;
  gap: 12px;
  padding: 12px;
  box-shadow: 5px 4px 8px #b9b9b9;
  border-radius: 8px;
  background-color: #ffffff;
}
.section-skills-row-title {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 18px;
}
.section-skills-row-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}
.section-skills-row-tag {
  display: inline-block;
  padding: 4px 12px;
  border-radius: 8px;
  background-color: #e1e1e1;
  cursor: default;
  transition: trasnform, opacity 0.1s ease-in-out;
  font-size: 18px;
  font-weight: 500;
  &:hover {
    transform: translateY(-2px);
    opacity: 0.8;
  }
}
@media all and (max-width: 1024px) {
  .section-skills-wrapper {
    grid-template-columns: repeat(2, 1fr);
    grid-row-gap: 24px;
  }
  .section-skills-row-title {
    font-size: 18px;
  }
  .section-skills-row-tag {
    font-size: 16px;
  }
}
@media all and (max-width: 640px) {
  .section-skills-wrapper {
    grid-template-columns: repeat(1, 1fr);
  }
  .section-skills-row-title {
    font-size: 16px;
  }
  .section-skills-row-tag {
    font-size: 14px;
  }
}
@media all and (max-width: 500px) {
  .section-skills {
    padding: 40px 0;
  }
}
</style>
