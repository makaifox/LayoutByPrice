<template>
  <!-- header -->
  <v-toolbar class="mt-5" flat>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <Searchbar />
    <v-btn rounded color="#E6E9FF" class="printbutton">
      <v-icon color="#2B9EDF">fas fa-print</v-icon>
      <span>Ver fila de impressão</span>
    </v-btn>

    <v-spacer></v-spacer>
    <v-btn rounded color="#4E5CDB" class="Createbutton">
      <v-icon color="#FFF">fas fa-plus</v-icon> <span>Criar Novo</span>
    </v-btn>
    <v-badge bordered top color="red" dot offset-x="10" offset-y="10">
      <v-btn icon dot offset-x="10" offset-y="10" class="bell">
        <v-icon>far fa-bell</v-icon>
      </v-btn>
    </v-badge>

    <v-avatar size="40" class="avatar">
      <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"></v-img>
    </v-avatar>
  </v-toolbar>
</template>

<script>
import Searchbar from "../components/Searchbar.vue";

export default {
  name: "MainBar",

  components: {
    Searchbar,
  },
  data: () => ({}),
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

.printbutton,
.Createbutton,
.bell,
.avatar {
  margin-bottom: 1rem;
}

.v-btn:not(.v-btn--round).v-size--default {
  height: auto;
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

.v-icon .notranslate .material-icons .theme--light {
  color: #2b9edf;
}
</style>