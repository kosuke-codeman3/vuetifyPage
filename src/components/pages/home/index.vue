<template>
  <v-app>
    <div>
      <v-app-bar color="primary">
        <v-toolbar-title class="white--text">LOGO</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn class="mx-2" fab light small @click="drawer = !drawer">
          <v-icon light>mdi-account</v-icon>
        </v-btn>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" absolute temporary right>
        <v-container class="d-flex flex-column justify-center align-center">
          <div
            class="user-icon pa-4 rounded-circle d-inline-block grey lighten-3"
          >
            <v-icon light>mdi-account</v-icon>
          </div>
          <div>USER NAME</div>
        </v-container>
        <v-list>
          <v-list-item-group>
            <v-list-item v-for="item in navListItems" :key="item.id">
              <v-list-item-title>{{ item.text }}</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </div>
    <v-main></v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    drawer: false,
    navListItems: [
      {
        id: 1,
        text: "LINK1",
      },
      {
        id: 2,
        text: "LINK2",
      },
      {
        id: 3,
        text: "LINK3",
      },
      {
        id: 4,
        text: "LINK4",
      },
    ],
  }),
};
</script>
