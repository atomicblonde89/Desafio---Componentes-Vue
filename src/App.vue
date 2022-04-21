<template>
  <div id="app" class="ms-4 my-5">
    <div>
      <Images @clickedResponse="clickChild" v-for="(imagen, i) in imagenes" :key="i" :imgperso="imagen" />
    </div>
    <span class="response"> <strong class="bg-danger">{{this.childResponse}}</strong></span>
  </div>
</template>

<script>
import Images from "./components/Images.vue"

export default {
  name: "App",
  data() {
    return {
      message: "Hola",
      childResponse: "",
      imagenes: [
        {
          nombre: "Rick Sanchez",
          src: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          nombre: "Morty Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          nombre: "Summer Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          nombre: "Beth Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          nombre: "Jerry Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
      ],
    };
  },
  components: {
    Images,
  },
  methods: {
    clickChild(childValue){
      this.childResponse=childValue;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  background-image: url(https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>