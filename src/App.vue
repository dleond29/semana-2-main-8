<template>
  <div id="app">

    <top-banner></top-banner>
    <services></services>
    <div class="container-fluid">
          <section-api></section-api>
    </div>
      
      <div class="container-fluid">
        <div class="row justify-content-center mb-5">
          <div class="col mt-5" v-for="(item, index) of team" :key="index">
            <team-card v-bind:member="item"></team-card>
          </div>
        </div>
      </div>

    <page-footer></page-footer>
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
import PageFooter from "./components/PageFooter.vue";
import TeamCard from "./components/TeamCard.vue";
import SectionApi from "./components/SectionApi.vue";
import TopBanner from './components/TopBanner.vue';
import Services from './components/Services'

export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    SectionApi,
    TopBanner,
    Services,
  },
  data() {
    return {
      title: "Vivo dentro de VUE",
      team: [
        {
          codigo: 1,
          nombre: "Diego León",
          descripcion: "1. Miembro equipo 8.",
          rol: "Desarrollador backend",
          imagen: "images/diegoL.png",
        },
        {
          codigo: 2,
          nombre: "Edwar Carrillo",
          descripcion: "2. Miembro equipo 8.",
          rol: "Desarrollador fronted",
          imagen: "images/edwarC.png",
        },
        {
          codigo: 3,
          nombre: "Jahir Rodríguez",
          descripcion: "3. Miembro equipo 8.",
          rol: "Desarrollador full stack",
          imagen: "images/jahirR.png",
        },
        {
          codigo: 4,
          nombre: "Andrés González",
          descripcion: "4. Miembro equipo 8.",
          rol: "Arquitecto de software",
          imagen: "images/andresG.png",
        },
        {
          codigo: 5,
          nombre: "Elmer Novoa",
          descripcion: "5. Miembro equipo 8.",
          rol: "Desarrollador junior",
          imagen: "images/elmerN.png",
        },
      ],
    };
  },
};
</script>

