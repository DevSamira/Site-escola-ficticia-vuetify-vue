<template>
  <v-app-bar color="white" dense class="fixed-bar">
    <img
      src="@/assets/images/logo.png"
      alt=""
      width="30rem"
      height="30rem"
      class="ml-4"
    />

    <v-toolbar-title class="ml-4" id="school">Escola Fictícia</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn color="red darken-4" dark v-bind="attrs" v-on="on">
          Seções</v-btn
        >
      </template>
      <v-list>
        <v-list-item
          style="cursor: pointer"
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title v-scroll-to="{ el: item.id }">{{
            item.title
          }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
    <div
      style="cursor: pointer"
      class="text-body-1 red--text text--darken-4 ml-12"
    >
      Alfabetização
    </div>
    <div
      style="cursor: pointer"
      class="text-body-1 red--text text--darken-4 ml-12"
    >
      Fundamental
    </div>
    <v-spacer></v-spacer>
  </v-app-bar>
</template>

<script>
export default {
  name: "NavbarComponent",
  data: () => ({
    items: [
      { title: "Quem somos", id: "#quemsomos" },
      { title: "Por que nossa escola?", id: "#porque" },
      { title: "Galeria", id: "#galeria" },
    ],
  }),
  computed: {
    width() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return 200;
        case "sm":
          return 400;
        case "md":
          return 500;
        case "lg":
          return 600;
        case "xl":
          return 800;
        default:
          return true;
      }
    },
  },
};
</script>

<style scoped>
</style>
