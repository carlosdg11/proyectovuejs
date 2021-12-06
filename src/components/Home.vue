<template>
  <v-layout text-center wrap>
    <v-flex mb-4>
      
      <h1 class="display-2 font-weight-bold">
        Tecnológico Nacional de México
      </h1>

      <h1 class="display-1 font-weight-bold text-center ">
        Campus Pinotepa
      </h1>

    </v-flex>

    <v-flex xs12>
      <v-img
        :src="require('../assets/logotec.png')"
        class="my-3"
        contain
        height="300"
      ></v-img>

      <h2 class="display-5 font-weight-bold text-center ">
        Bienvenidos
      </h2>

    </v-flex>

  </v-layout>
  

</template>

<script>
export default {};
</script>

<style scoped>
h1 {
  margin-top: 30px;
  margin-bottom: 30px;
  color: #020344;
}

h2 {
  margin-top: 30px;
  font-size: 35px;
  color: #BE0606;
}

</style>
