<template>
  <div class="grey" id="porque">
    <div
      class="mt-8 pt-6 white--text text-center text-h4 pa-4 pb-12"
      height="5rem"
    >
      <span class="material-icons"> menu_book </span>
      Por que nossa escola?
      <div class="red-bar red darken-4 mt-2"></div>
    </div>
    <v-row justify="d-flex mt-6 justify-center align-center">
      <div>
        <v-img
          lazy-src="@/assets/images/studyinghand.jpg"
          max-height="300"
          max-width="300"
          src="@/assets/images/girl.png"
        ></v-img>
      </div>
      <section>
        <div class="text-h6 text-right" v-for="(item, i) in motives" :key="i">
          <strong class="circle">°</strong>
          {{ item.motive }}
          <span class="material-icons"> check_circle </span>
          <v-spacer></v-spacer>
        </div>
      </section>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "PorQueComponent",
  data: () => ({
    motives: [
      { motive: "Metodologia humanizada" },
      { motive: "Profissionais capacitados" },
      { motive: "Sempre revolucionando" },
      { motive: "Incentivo à pesquisa, artes e esportes" },
      { motive: "Câmera de segurança em todas as salas" },
    ],
  }),
};
</script>

<style scoped>
.red-bar {
  height: 0.3rem;
  width: 18rem;
  margin: 0 auto;
  border-radius: 4rem;
}
.circle {
  color: brown;
}
</style>