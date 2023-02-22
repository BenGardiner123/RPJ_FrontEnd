<template>
  <div class="project-display-container">
    <div class="project-section">
      <h3>Front End:</h3>
      <v-icon class="tech-icon">{{ icons.angular }}</v-icon>
    </div>
    <div class="project-section">
      <h3>Middle/API:</h3>
      <v-icon class="tech-icon">{{ icons.vue }}</v-icon>
    </div>
    <div class="project-section">
      <h3>Back End:</h3>
      <Icon icon="ant-design:console-sql-outlined" />
    </div>
    <div class="project-description">
      <p>{{ projectDescription }}</p>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";
export default {
  name: "ProjectDisplay",
  components: {
    Icon,
  },
  props: {
    frontEndIcon: {
      type: String,
      required: true,
    },
    middleApiIcon: {
      type: String,
      required: true,
    },
    backEndIcon: {
      type: String,
      required: true,
    },
    projectDescription: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      icons: {
        vue: "mdi-vuejs",
        react: "mdi-react",
        angular: "mdi-angular",
        node: "mdi-nodejs",
        python: "mdi-language-python",
        java: "mdi-language-java",
        csharp: "mdi-language-csharp",
        sql: "mdi-database",
        mongo: "mdi-database",
        firebase: "mdi-database",
      },
    };
  },
};
</script>

<style scoped>
.project-display-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  margin-top: 50px;
  width: 60vw;
  margin: auto;
}

.project-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  height: 100px;
}

.tech-icon {
  font-size: 50px;
}

.project-description {
  margin-top: 50px;
  text-align: center;
}
</style>
