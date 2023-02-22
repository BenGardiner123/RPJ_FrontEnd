<template>
  <div class="search-container">
    <v-autocomplete
      class="search-input"
      v-model="searchText"
      :items="[
        'California',
        'Colorado',
        'Florida',
        'Georgia',
        'Texas',
        'Wyoming',
      ]"
      variant="solo"
      prepend-inner-icon="mdi-magnify"
    >
    </v-autocomplete>

    <v-btn
      class="search-button"
      rounded="pill"
      size="x-large"
      variant="flat"
      color="secondary"
      @click="search"
    >
      go baby go!
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "SearchInput",
  data() {
    return {
      searchText: "",
      placeholderText: "Enter search terms",
    };
  },
  methods: {
    search() {
      // Implement search functionality here
    },
  },
};
</script>

<style scoped>
.search-container {
  display: flex;
  flex-direction: row;

  /* background-color: gray; */
  width: 60vw;
  margin: auto;
}

.search-input .v-input__control {
  width: 75%;
  /* Set the input height to the value of $input-control-height */
  /* height: 100%; */
}
.search-button .v-btn__content {
  /* Set the minimum height */
  /* min-height: 200px; */
}
</style>
