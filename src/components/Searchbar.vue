              <template>
  <v-badge bordered top color="#4E5CDB" dot offset-x="10" offset-y="10">
    <v-autocomplete
      v-model="searchString"
      :disabled="isUpdating"
      solo
      chips
      color="#4E5CDB"
      label="O que você deseja ?"
      item-text="name"
      item-value="name"
      multiple
      clearable
      append-icon="search"
      :append-icon-cb="helo"
      :open-on-click="false"
    >
      <v-list-tile>
        <v-list-tile-title> procurando.... </v-list-tile-title>
      </v-list-tile>
    </v-autocomplete>
  </v-badge>
</template>

<style>
.v-input__control {
  border-radius: 2rem !important;
  width: 20rem;
  margin: 0 !important;
}
.v-input__slot {
  box-shadow: none !important;
  border: solid 1px #d5d5d5;
  margin: 0 !important;
  padding: 0 1.5rem;
}
.theme--light.v-text-field > .v-input__control > .v-input__slot:before {
  border: none;
}

.v-text-field__details {
  padding: 0 !important;
  margin: 0 !important;
}
</style>