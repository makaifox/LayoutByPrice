<template>
  <v-navigation-drawer v-model="drawer" permanent color="#4E5CDB" app>
    <v-list-item class="px-2 py-5">
      <v-list-item-title class="text-capitalize" align="center">
        <img src="../assets/logo.png" alt="logo" class="logo" />
        ByPrice
      </v-list-item-title>
    </v-list-item>
    <v-list-item class="px-2 py-5">
      <v-btn rounded color="#FFF" class="selectButton">
        <span>Loja - Água Verde</span>
        <v-icon class="select-ico">fas fa-chevron-down</v-icon>
      </v-btn>
    </v-list-item>
    <v-list nav dense>
      <v-list-item-group v-model="selectedItem" color="#080E3D">
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <template v-slot:append>
      <div class="pa-2 help" align="center">ajuda</div>
    </template>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    drawer: null,
    items: [
      { icon: "fas fa-home", text: "Dashboard", route: "/home" },
      { icon: "fas fa-book-open", text: "Templates", route: "/Templates" },
      { icon: "fas fa-shopping-bag", text: "Campanhas", route: "/campain" },
      { icon: "fas fa-tags", text: "Arte Avulsa", route: "/arts" },
      { icon: "fas fa-print", text: "Fila de Impressão", route: "/print" },
      {
        icon: "fas fa-cloud-download-alt",
        text: "Download",
        route: "/download",
      },
      { icon: "fas fa-cog", text: "Configurações", route: "/config" },
    ],
  }),
};
</script>
<style scoped>
.v-list-item__title,
.v-icon,
.help {
  font: Nunito !important;
  color: #ffffff !important;
}
div >>> .v-list a {
  text-decoration: none;
}
.logo {
  max-height: 2rem;
}

.select-ico,
selectButton span {
  color: #080e3d !important;
  padding: 0 1rem;
}
</style>

