<template>
  <div>
    <Header
      :nlogin="$store.state.nombreLogin"
      :var1="$store.state.loginOK"
    ></Header>
    <!-- Carousel Bootstrap -->
    <div id="demo" class="carousel slide" data-bs-ride="carousel">
      <!-- Indicators/dots -->
      <div class="carousel-indicators">
        <button
          type="button"
          data-bs-target="#demo"
          data-bs-slide-to="0"
          class="active"
        ></button>
        <button
          type="button"
          data-bs-target="#demo"
          data-bs-slide-to="1"
        ></button>
        <button
          type="button"
          data-bs-target="#demo"
          data-bs-slide-to="2"
        ></button>
      </div>

      <!-- The slideshow/carousel -->
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="./img/libros.jpg" class="d-block" style="width: 100%" />
        </div>
        <div class="carousel-item">
          <img src="./img/banner.jpg" class="d-block" style="width: 100%" />
        </div>
        <div class="carousel-item">
          <div
            class="container-fluid p-5 bg-dark text-white"
            style="height: 400px"
          >
            <h1>Tablero de anuncios</h1>
            <p>
              En este párrafo se puede agregar cualquier información relevante
              para la biblioteca.<br />
              Puede contener información de actividades próximas a realizar e
              información de interés general para la comunidad a la que esté
              dirigida la página.<br />
              Con esto se comprueba que podemos agregar cualquier tipo de
              elementos en el slider.
            </p>
          </div>
        </div>
      </div>

      <!-- Left and right controls/icons -->
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#demo"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon"></span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#demo"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon"></span>
      </button>
    </div>
    <br />

    <div>
      <h1>Servicios</h1>
      <!-- inicio sección de servicios -->
      <div id="servicios" class="services-section">
        <article class="services-info">
          <img class="services-info__imagen" src="./img/loan.png" alt="" />
          <h2 class="services-info__title">
            <router-link to="/simulador">Simulador</router-link>
          </h2>
          <p class="services-info__text">
            En esta sección podrás simular las cuotas de tu prestamo bancario y
            evaluar su solicitud
          </p>
        </article>
        <article class="services-info">
          <img class="services-info__imagen" src="./img/logocurso.png" alt="" />
          <h2 class="services-info__title">
            <router-link to="/cursos">Cursos</router-link>
          </h2>
          <p class="services-info__text">
            En esta sección podrás encontrar todo los cursos disponibles y los
            cursos ya finalizados.
          </p>
        </article>
        <article class="services-info">
          <img
            class="services-info__imagen"
            src="./img/logolibros.png"
            alt=""
          />
          
          <h2 class="services-info__title">
            <router-link to="/prestamos">Préstamos</router-link>
          </h2>
          <p class="services-info__text">
            En esta sección podrás acceder a los servicios relacionados con los
            libros disponibles.
          </p>
        </article>
      </div>
      <!-- fin sección de servicios -->
      <h1>Noticias</h1>
      <!-- inicio sección de noticias -->
      <div id="news" class="news-section">
        <article class="news-info">
          <div class="news-header">
            <img
              class="news-info__image"
              src="https://cdn.vuetifyjs.com/images/cards/house.jpg"
              alt=""
            />
            <h2 class="news-info__title">Startups: Perspectivas futuras</h2>
          </div>
          <p class="news-info__text">
            Triunfarán aquellas startups que ofrezcan soluciones a través de
            tecnologías como Big Data, impresión 3D, robótica, realidad
            aumentada, Internet de las Cosas, Blockchain...<a
            >
              Ver más</a
            >
          </p>
        </article>

        <article class="news-info">
          <div class="news-header">
            <img
              class="news-info__image"
              src="https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg"
              alt=""
            />
            <h2 class="news-info__title">
              La desertificación acaba con los bosques
            </h2>
          </div>
          <p class="news-info__text">
            Los jóvenes de la generación climática elaboran un plan de choque
            para contrarrestar la deforestación. En la medida de lo posible...<a
              >Ver más</a
            >
          </p>
        </article>

        <article class="news-info">
          <div class="news-header">
            <img
              class="news-info__image"
              src="https://cdn.vuetifyjs.com/images/cards/road.jpg"
              alt=""
            />
            <h2 class="news-info__title">
              Desertificación: Estrategias para enfrentarla
            </h2>
          </div>
          <p class="news-info__text">
            Las respuestas a la crisis climática hace un uso eficiente de los
            recursos, con una apuesta estratégica decidida del conjunto de las
            administraciones públicas...
            <a> Ver más</a>
          </p>
        </article>

        <article class="news-info">
          <div class="news-header">
            <img
              class="news-info__image"
              src="https://cdn.vuetifyjs.com/images/cards/plane.jpg"
              alt=""
            />
            <h2 class="news-info__title">Nuevas tecnologías: Aerolíneas</h2>
          </div>
          <p class="news-info__text">
            El branding se reinventa continuamente para volver a empezar de
            nuevo. El CMO cierra una ronda inicial de 10M $, mediante el informe
            correspondiente...
            <a> Ver más</a>
          </p>
        </article>
      </div>
      <!-- fin sección de noticias -->
    </div>
    <div>
      <!-- Inicio sección integrantes -->
      <h1>Equipo 7 - Grupo 32</h1>
      <v-row>
        <v-col>
          <v-card class="mx-auto" max-width="344">
            <v-img src="./img/Sebastian B.png" height="200px"></v-img>
            <v-card-title>Sebastian Barrera</v-card-title>
            <v-card-subtitle>Scrum Master</v-card-subtitle>
          </v-card>
        </v-col>

        <v-col>
          <v-card class="mx-auto" max-width="344">
            <v-img src="./img/Carolina.png" height="200px"></v-img>
            <v-card-title>Carolina Cova</v-card-title>
            <v-card-subtitle>Product Owner</v-card-subtitle>
          </v-card>
        </v-col>

        <v-col>
          <v-card class="mx-auto" max-width="344">
            <v-img
              src="./img/Sebastian R.png"
              height="200px"
              position = "50% 25%"
            ></v-img>
            <v-card-title>Sebastian Renteria</v-card-title>
            <v-card-subtitle>Development team</v-card-subtitle>
          </v-card>
        </v-col>

        <v-col>
          <v-card class="mx-auto" max-width="344">
            <v-img src="./img/Diego.png" height="200px"></v-img>
            <v-card-title>Diego Guisao</v-card-title>
            <v-card-subtitle>Development team</v-card-subtitle>
          </v-card>
        </v-col>

        <v-col>
          <v-card class="mx-auto" max-width="344">
            <v-img
              src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
              height="200px"
            ></v-img>
            <v-card-title>Santiago Puello</v-card-title>
            <v-card-subtitle>Development team</v-card-subtitle>
          </v-card>
        </v-col>
      </v-row>

      <!-- Fin sección integrantes -->
    </div>
    <br />
    <br />
    <!-- Inicio pie del sitio -->
    <Footer />
  </div>
</template>

<script>
import Footer from "./Footer.vue";
import Header from "./Header.vue";
export default {
  name: "PaginaInicio",
  components: { Header, Footer },
  data: () => ({
    cards: [
      {
        title: "Startups: Perspectivas futuras",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        resume:
          "Triunfarán aquellas startups que ofrezcan soluciones a través de tecnologías como Big Data, impresión 3D, robótica, realidad aumentada, Internet de las Cosas, Blockchain o ciberseguridad...",
        flex: 6,
      },
      {
        title: "La desertificación acaba con los bosques del Amazonas",
        src: "https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg",
        resume:
          "Los jóvenes de la generación climática elaboran un plan de choque para contrarrestar la deforestación. En la medida de lo posible...",
        flex: 6,
      },
      {
        title: "Desertificación: Estrategias para enfrentarla",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        resume:
          "Las respuestas a la crisis climática hace un uso eficiente de los recursos, con una apuesta estratégica decidida del conjunto de las administraciones públicas, así como la implicación y compromiso del conjunto de los agentes económicos y sociales...",
        flex: 6,
      },
      {
        title: "Nuevas tecnologías: Aerolíneas",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        resume:
          "El branding se reinventa continuamente para volver a empezar de nuevo. El CMO cierra una ronda inicial de 10M €, mediante el informe correspondiente...",
        flex: 6,
      },
    ],
  }),
  methods: {},
};
</script>

<style>
* {
  box-sizing: border-box;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
body {
  max-width: 1400px;
  min-width: 375px;
  margin-right: auto;
  margin-left: auto;
  margin-top: 0;
  margin-bottom: 0;
  color: #222222;
}
p {
  text-transform: none;
}
.center {
  padding: 70px 0;
  width: 50%;
}
.header-section {
  margin-bottom: 100px;
}
.header-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  text-align: center;
}
.site-title {
  width: 30%;
}
.site-nav {
  width: 40%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.site-nav > a {
  color: inherit;
  text-decoration: none;
}
.site-nav > a:hover {
  text-decoration: underline;
  font-weight: bold;
}
.logo-container {
  width: 30%;
}
.logo-container__site-logo {
  height: 80px;
}
.banner {
  width: 100%;
}
.banner > img {
  width: 100%;
  height: 400px;
  max-width: 1400px;
  object-fit: cover;
}
/* inicio slider con imágenes*/
ul,
li {
  padding: 0;
  margin: 0;
  list-style: none;
}
ul.slider {
  position: relative;
  width: 100%;
  height: 400px;
  max-width: 1400px;
  object-fit: cover;
}
ul.slider li {
  position: absolute;
  left: 0px;
  top: 0px;
  opacity: 0;
  width: inherit;
  height: inherit;
  transition: opacity 0.5s;
  background: #fff;
}
ul.slider li img {
  width: 100%;
  height: 400px;
  max-width: 1400px;
  object-fit: cover;
}
ul.slider li:first-child {
  opacity: 1;
  /*se muestra el primer <li>*/
}
ul.slider li:target {
  opacity: 1;
  /*se muestra el <li> del enlace que pulsemos*/
}
.menu {
  text-align: center;
  margin: 20px;
}
.menu li {
  display: inline-block;
  text-align: center;
}
.menu li a {
  display: inline-block;
  color: #222222;
  text-decoration: none;
  background-color: #089dc2;
  width: 20px;
  height: 20px;
  font-size: 15px;
  border-radius: 200%;
}
/* fin slider con imágenes*/
.services-section,
.seccion-equipo {
  display: flex;
  margin-bottom: 100px;
}
.header-container {
  background-color: #089dc2;
}
/* Estilos de la sección de Noticias */
.news-section {
  flex-wrap: wrap;
  display: flex;
}
.news-info {
  width: 50%;
  padding: 10px;
}
.news-info__image {
  width: 650.88px;
  height: 300.5px;
  border-radius: 1.5rem;
}
.news-info__text {
  justify-content: center;
}
.news-header {
  display: block;
  justify-content: space-around;
}
.news-info__title {
  align-self: center;
  height: 38px;
}
.v-toolbar__title.noticias {
  color: #fff;
}
/* Fin de Estilos en la sección de noticias */
.services-info {
  padding: 20px;
  text-align: center;
}
.seccion-pie {
  background-color: #25294f;
  height: 270px;
  display: flex;
  color: white;
  justify-content: space-evenly;
}
.services-info__imagen {
  border-radius: 50%;
  margin-right: auto;
  margin-left: auto;
}
.team-info {
  width: 25%;
  padding: 15px;
}
.team-info__imagen {
  display: block;
  margin-right: auto;
  margin-left: auto;
}
</style>