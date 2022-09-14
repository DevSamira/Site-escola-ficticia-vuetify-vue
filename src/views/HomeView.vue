<template>
  <div color="white">
    <NavbarComponent />
    <img
      src="@/assets/images/jumpkids.jpg"
      alt=""
      width="100%"
      height="590rem"
    />
    <QuemSomosComponent />
    <PorQueComponent />
    <GaleriaComponent />
  </div>
</template>

<script>
import NavbarComponent from "../components/NavbarComponent";
import QuemSomosComponent from "../components/QuemSomosComponent";
import PorQueComponent from "../components/PorQueComponent.vue";
import GaleriaComponent from "../components/GaleriaComponent.vue";

export default {
  name: "HomeView",

  components: {
    NavbarComponent,
    QuemSomosComponent,
    PorQueComponent,
    GaleriaComponent,
  },
};
</script>
