<template>
  <div class="project-display-container">
    <div class="project-section">
      <h3>Front End:</h3>
      <img src="https://img.icons8.com/officel/80/null/react.png" />
    </div>
    <div class="project-section">
      <h3>Middle/API:</h3>
      <!-- <v-icon class="tech-icon">{{ middleApiIcon }}</v-icon> -->
      <img src="https://img.icons8.com/color/48/null/net-framework.png" />
    </div>
    <div class="project-section">
      <h3>Back End:</h3>
      <!-- <v-icon class="tech-icon">{{ backEndIcon }}</v-icon> -->
      <img
        src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/null/external-sql-mobile-app-development-flaticons-lineal-color-flat-icons.png"
      />
    </div>
    <div class="project-description">
      <p>{{ projectDescription }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectDisplay",
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
};
</script>

<style scoped>
.project-display-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin-top: 50px;
}

.project-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
}

.tech-icon {
  font-size: 50px;
}

.project-description {
  margin-top: 50px;
  text-align: center;
}
</style>
