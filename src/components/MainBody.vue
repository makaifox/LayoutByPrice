<template>
  <v-container fluid>
    <v-container fluid>
      <v-row>
        <v-col>
          <span class="caption">Configurações</span>
          <br />
          <h1>Usuários</h1>
          <span class="caption">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed dapibus
            scelerisque nisi eget pulvinar.</span
          >
          <br />
          <br />
          <v-btn rounded color="#4E5CDB" class="adduser">
            <v-icon color="#FFF">fas fa-plus</v-icon>
            <span>Adicionar novo usuário</span>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row>
        <v-card
          class="mx-auto table-collum"
          outlined
          v-for="item in user"
          :key="item.name"
        >
          <v-simple-table>
            <template v-slot:default>
              <thead>
                <tr>
                  <th class="text-left">
                    <v-tab>
                      <v-btn fab color=" lighten-4" elevation="0"
                        >{{ item.number }}
                      </v-btn>
                    </v-tab>
                  </th>
                  <th class="text-left">
                    <v-tab>
                      <v-btn fab color=" lighten-4" elevation="0">
                        {{ item.button }}
                      </v-btn>
                    </v-tab>
                  </th>
                  <th class="text-left">{{ item.name }}</th>
                  <th class="spacerline"></th>
                  <th class="text-left">{{ item.email }}</th>
                  <th class="text-left">
                    <v-btn rounded color="#4E5CDB" class="permissions">
                      <span>Permissões</span>
                    </v-btn>
                  </th>
                  <th class="text-left">
                    <v-icon color="red">fas fa-trash-alt</v-icon>
                  </th>
                </tr>
              </thead>
            </template>
          </v-simple-table>
        </v-card>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: "MainBody",
  data() {
    return {
      user: [
        {
          number: "001",
          button: "RA",
          name: "Rafael Álvarez",
          email: "rafaelalv@cooper.com.br",
        },
        {
          number: "001",
          button: "RA",
          name: "Rafael Álvarez",
          email: "rafaelalv@cooper.com.br",
        },
        {
          number: "001",
          button: "RA",
          name: "Rafael Álvarez",
          email: "rafaelalv@cooper.com.br",
        },
      ],
    };
  },
};
</script>

<style>
.table-collum {
  margin: 1rem 0;
}
.v-data-table {
  padding: 0.5 rem;
}
.v-sheet.v-card {
  border-radius: 11px !important;
  border: 0.30000001192092896px solid #bcbecc !important;
  padding: 0.8rem;
  opacity: 1;
}

.theme--light.v-data-table
  > .v-data-table__wrapper
  > table
  > thead
  > tr:last-child
  > th {
  border-bottom: none;
}

.spacerline {
  padding: 0 2rem;
}
.permissions,
.adduser {
  color: #fff !important;
}
.permissions span,
.adduser span {
  padding: 1rem;
}

.container {
  margin: 1rem;
  padding: 0.5rem;
}
</style>