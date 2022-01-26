<template>
  <div class="home">
    .

    <!-- header -->

    <MainBar />
    <v-divider></v-divider>
  </div>
</template>

<script>
import MainBar from "../components/MainBar.vue";

export default {
  name: "Home",

  components: {
    MainBar,
  },
  data: () => ({
    tab: null,
    text: "center",
    fill: true,
    padding: 8,
    radius: 10,
    value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0],
    width: 2,
    lineCap: "round",
    type: "trend",
    autoLineWidth: false,
    fills: false,
  }),
};
</script>
<style lang="sass" scoped>
.v-card.on-hover.theme--dark
  background-color: rgba(#FFF, 0.8)
  >.v-card__text
    color: #000
</style>
<style scoped>
.border {
  border-right: 1px solid grey;
}

.bell {
  background-color: #e6e9ff !important;
  border-radius: 1rem !important;
}

.v-badge,
.printbutton,
.Createbutton {
  margin: 0 2rem;
}

.printbutton {
  color: #2b9edf !important;
  border: none;
  box-shadow: none;
  padding: 2rem 0;
}

.Createbutton {
  color: #fff !important;
}

.printbutton span,
.Createbutton span {
  padding: 1rem;
}
</style>