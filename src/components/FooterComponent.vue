<template>
  <v-footer padless class="mt-16" color="red darken-4">
    <v-card flat tile class="red darken-4 white--text text-center ma-auto">
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text text-center">
        Educamos nossos alunos com amor, para que o mundo seja transformado e a
        humanidade prevaleça acompanhada da liberdade que o conhecimento
        proporciona.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>&copy; DevSamira</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
  }),
};
</script>

<style>
</style>