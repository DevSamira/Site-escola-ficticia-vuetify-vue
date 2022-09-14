<template>
  <div>
    <v-card
      class="mx-auto mt-11 mb-2 red white--text rounded-xl"
      elevation="15"
      max-width="344"
      style="cursor: pointer"
    >
      <v-img
        :src="require('@/assets/images/' + imageName)"
        height="200px"
      ></v-img>
      <div class="d-flex align-center">
        <span class="material-icons"> arrow_right </span>
        <v-card-title> {{ Ptitle }} </v-card-title>
      </div>
      <v-card-subtitle class="white--text text-decoration-underline">
        {{ Psubtitle }}
      </v-card-subtitle>

      <v-card-actions>
        <v-spacer></v-spacer>

        <v-btn icon @click="show = !show" height="1rem">
          <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>

          <v-card-text>
            {{ Ptextdesc }}
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  props: {
    Ptitle: String,
    Psubtitle: String,
    Ptextdesc: String,
    imageName: String,
  },
  data: () => ({
    show: false,
  }),
};
</script>

<style>
</style>