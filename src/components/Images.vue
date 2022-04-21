<template>
  <div class="d-flex mt-4">
    <div>
      <img
        :src="imgperso.src"
        :alt="imgperso.nombre"
        class="img-rick"
        width="120"
      />       
<p class="d-inline ms-3 name-rick">{{ imgperso.nombre }}</p>
    </div>
     <div>
      <b-button variant="outline-success" class="hello-response" @click="clickResponse">Quotes</b-button>
    </div>
  
  </div>
</template>

<script>
export default {
  name: "ImagenRick",
  props: {
    imgperso: {
      type: Object,
      default: () => {},
    },
    message: {
      type:String,
      required: true,
    }
  },
  methods: {
    clickResponse(){
      this.$emit("clickedResponse", "Wubba Lubba Dub Dub!!!")
    }
  }
};
</script>
 
<style>
.name-rick {
  font-size: 40px;
  font-family: cursive;
  color: deepskyblue;
}
.img-rick {
  border-radius: 50%;
  width: 120px;
}
</style>