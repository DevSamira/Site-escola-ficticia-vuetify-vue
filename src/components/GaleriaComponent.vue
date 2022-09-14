<template>
  <div id="galeria">
    <div class="text-h3 text-center mr-6 red--text text--darken-4 mt-12">
      Galeria
    </div>
    <v-container class="d-sm-flex align-center justify-center mt-4 px-2">
      <v-card elevation="24" width="400" class="rounded-xl mt-4 ma-auto py-4">
        <v-system-bar lights-out></v-system-bar>
        <v-carousel
          :continuous="false"
          :cycle="cycle"
          :show-arrows="false"
          hide-delimiter-background
          delimiter-icon="mdi-minus"
          height="300"
        >
          <v-carousel-item
            v-for="(item, i) in items"
            :key="i"
            :src="item.src"
          ></v-carousel-item>
        </v-carousel>
        <v-list two-line>
          <v-list-item>
            <v-list-item-avatar class="rounded-0" width="2rem">
              <v-img src="@/assets/images/logo.png"></v-img>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title>Dia de passeio</v-list-item-title>
              <v-list-item-subtitle>4° ano</v-list-item-subtitle>
            </v-list-item-content>
            <v-icon color="red darken-4" large class="material-icons">
              directions_bus
            </v-icon>
          </v-list-item>
        </v-list>
      </v-card>
      <v-card elevation="24" width="400" class="rounded-xl mt-4 ma-auto py-4">
        <v-system-bar lights-out></v-system-bar>
        <v-carousel
          :continuous="false"
          :cycle="cycle"
          :show-arrows="false"
          hide-delimiter-background
          delimiter-icon="mdi-minus"
          height="300"
        >
          <v-carousel-item
            v-for="(item, i) in feiraciencias"
            :key="i"
            :src="item.src"
          ></v-carousel-item>
        </v-carousel>
        <v-list two-line>
          <v-list-item>
            <v-list-item-avatar class="rounded-0" width="2rem">
              <v-img src="@/assets/images/logo.png"></v-img>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title>Feira de ciências 2022</v-list-item-title>
              <v-list-item-subtitle>Por Smart's</v-list-item-subtitle>
            </v-list-item-content>
            <v-icon color="red darken-4" large class="material-icons">
              science
            </v-icon>
          </v-list-item>
        </v-list>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "GaleriaComponent",
  data() {
    return {
      items: [
        {
          src: require("@/assets/images/passeio-escolar/passeio-escolar-1.jpg"),
        },
        {
          src: require("@/assets/images/passeio-escolar/passeio-escolar-2.jpg"),
        },
        {
          src: require("@/assets/images/passeio-escolar/passeio-escolar-3.jpg"),
        },
        {
          src: require("@/assets/images/passeio-escolar/passeio-escolar-4.jpg"),
        },
        {
          src: require("@/assets/images/passeio-escolar/passeio-escolar-5.jpeg"),
        },
      ],
      feiraciencias: [
        {
          src: require("@/assets/images/feira-de-ciencias/feira-1.jpg"),
        },
        {
          src: require("@/assets/images/feira-de-ciencias/feira-2.jpg"),
        },
        {
          src: require("@/assets/images/feira-de-ciencias/feira-3.jpg"),
        },
        {
          src: require("@/assets/images/feira-de-ciencias/feira-4.jpg"),
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>