<template>
  <div id="app">
    <top-banner></top-banner>
    <div class="container-fluid">
      <noticias></noticias>
    </div>
    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card :member="item"></team-card>
        </div>
      </div>
    </div>
    <page-footer></page-footer>
  </div>
</template>

<script>
import Noticias from "./components/Noticias.vue";
import TeamCard from "./components/TeamCard.vue";
import PageFooter from "./components/PageFooter.vue";
import TopBanner from "./components/TopBanner.vue";
export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    Noticias,
    TopBanner,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "Jean Pierre Rojas",
          descripcion: "Ingeniero Electrónico - Universidad Surcolombiana",
          rol: "Scrum master",
          image: require("./assets/jean.jpg"),
        },
        {
          codigo: 2,
          nombre: "Walter González",
          descripcion:
            "Estudiante de Ingeniería de Sistemas - Universidad Nacional Abierta y a Distancia",
          rol: "Desarrollador",
          image: require("./assets/walter.jpg"),
        },
        {
          codigo: 3,
          nombre: "Marcela Silva",
          descripcion:
            "Ingeniera en Telecomunicaciones - Unidades Tecnológicas de Santander",
          rol: "Desarrollador",
          image: require("./assets/marcela.jpg"),
        },
        {
          codigo: 4,
          nombre: "Sergio Davil Romero",
          descripcion:
            "Ingeniero Mecánico - Universidad Industrial de Santander",
          rol: "Desarrollador",
          image: require("./assets/sergio.jpg"),
        },
      ],
    };
  },
};
</script>

