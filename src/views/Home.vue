<template>
  <div class="home">
    .

    <!-- header -->

    <MainBar />
    <v-divider></v-divider>

    <!-- Body -->
    <MainBody />
  </div>
</template>

<script>
import MainBar from "../components/MainBar.vue";
import MainBody from "../components/MainBody.vue";

export default {
  name: "Home",

  components: {
    MainBar,
    MainBody,
  },
  data: () => ({}),
};
</script>

<style scoped>
</style>