<template>
  <div id="quemsomos">
    <div
      class="pt-6 grey white--text text-center text-h4 pa-4 pb-12"
      height="5rem"
    >
      <span class="material-icons"> menu_book </span>
      Quem somos?
      <div class="red-bar red darken-4 mt-2"></div>
    </div>
    <v-container class="d-md-flex">
      <card-component
        Ptitle="Escola particular de ensino "
        Psubtitle="Há dez anos na ativa!"
        Ptextdesc="Há mais de 10 anos contribuímos para a educação em Cajazeiras-PB."
        imageName="dez-anos.jpg"
      />
      <v-spacer></v-spacer>
      <card-component
        Ptitle="Localização "
        Psubtitle="Centro - Cajazeiras-PB"
        Ptextdesc="Rua: xxxxxxx xx xxxxx, n° xx. Próximo à catedral"
        imageName="cajacentro.jpg"
      />
      <v-spacer></v-spacer>
      <card-component
        Ptitle="Venha nos visitar!"
        Psubtitle="Funcionamos de 6:00 às 17:30"
        Ptextdesc="Ficaremos felizes em recebê-lo :)"
        imageName="horario.png"
      />
    </v-container>
  </div>
</template>

<script scoped>
import CardComponent from "./CardComponent.vue";

export default {
  name: "QuemSomosComponent",
  components: {
    CardComponent,
  },
  data: () => ({}),
};
</script>

<style scoped>
div {
  background-color: #fff;
}

.red-bar {
  height: 0.3rem;
  width: 11rem;
  margin: 0 auto;
  border-radius: 4rem;
}
</style>