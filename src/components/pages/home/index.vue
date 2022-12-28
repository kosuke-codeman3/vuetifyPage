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
    <v-main>
      <v-carousel v-model="model">
        <v-carousel-item>
          <v-img src="../../../../public/img/image1.jpg" height="100%"></v-img>
        </v-carousel-item>
        <v-carousel-item>
          <v-img src="../../../../public/img/image2.jpg" height="100%"></v-img>
        </v-carousel-item>
        <v-carousel-item>
          <v-img src="../../../../public/img/image3.jpg" height="100%"></v-img>
        </v-carousel-item>
      </v-carousel>
      <v-container>
        <v-row>
          <v-col>
            <v-card>
              <v-card-title>HEAD1</v-card-title>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
            </v-card>
          </v-col>
          <v-col>
            <v-card>
              <v-card-title>HEAD2</v-card-title>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
            </v-card>
          </v-col>
          <v-col>
            <v-card>
              <v-card-title>HEAD3</v-card-title>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <v-card class="overflow-hidden">
              <v-card-title>HEAD4</v-card-title>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
            </v-card>
          </v-col>
          <v-col>
            <v-card class="overflow-hidden">
              <v-card-title>HEAD5</v-card-title>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
            </v-card>
          </v-col>
          <v-col>
            <v-card class="overflow-hidden">
              <v-card-title>HEAD6</v-card-title>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col>
            <v-card>
              <v-card-title>CARD 1</v-card-title>
              <v-card-subtitle>about</v-card-subtitle>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
              <v-card-actions>
                <v-btn small>OK</v-btn>
                <v-btn small>Cancel</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col>
            <v-card>
              <v-card-title>CARD 2</v-card-title>
              <v-card-subtitle>about</v-card-subtitle>
              <v-card-text>
                sample Text sample Text sample Text sample Text sample Text
                sample Text sample Text sample Text sample Text sample Text
                sample Text
              </v-card-text>
              <v-card-actions>
                <v-btn small>OK</v-btn>
                <v-btn small>Cancel</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-footer color="primary">
      <v-row
      justify="center"
      no-gutters
      >
      <v-btn
        v-for="link in navListItems"
        :key="id"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link.text }}
      </v-btn>
      <v-col
        class="primary py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
    </v-footer>
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
