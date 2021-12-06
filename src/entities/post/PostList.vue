<template>
  <div>
    <div class="float-right">
      <v-btn v-if="isAdmin" :to="{ name: 'PostCreate' }" color="primary">
        New
      </v-btn>
    </div>
    <div class="text-center clear">
      <h2>Publicaciones del Blog</h2>
      </div>

      <div class="text-center">
      <h3 class="display-1 font-weight-bold">Vue-CLI y Comandos Básicos</h3>

      <p>
      Vue tiene su <strong>vue-cli</strong>, es decir la interfaz de línea de comandos de 
      Vue que es una herramienta creada por el equipo de Vue para ayudar 
      con la creación del scaffolding y la configuración inicial del proyecto. <br>
      Para poder utilizar el <strong>vue-cli</strong> es necesario tener instalado <strong>Node.js</strong> en nuestro
       equipo ya que la instalación se realiza a través de npm con el siguiente comando.
      </p>

      <div class="comand">
      <span>
      npm install -g @vue/cli
      </span>
      </div>

      <p class="text2">
      Este comando hace una instalación global del cli en nuestro equipo y nos habilita el
      uso del comando siguiente para la creación del proyecto.
      </p>

      <div class="comand">
      <span>
      vue create my-project
      </span>
      </div>

      <p class="text2">
      Este comando hace una instalación global del cli en nuestro equipo y nos habilita el
      uso del comando siguiente para la creación del proyecto.
      </p>

      <div class="comand">
      <span>
      npm run serve
      </span>
      </div>

      <p class="text2">
      El cual nos genera una instancia local del servidor para poder ejecutar nuestra aplicación.
      </p>

      <iframe class="video1"  width="750" height="415" src="https://www.youtube.com/embed/e8xBCik4fIk" title="YouTube 
      video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; 
      gyroscope; picture-in-picture" allowfullscreen></iframe>

      <h4 class="display-1 font-weight-bold">Funcionalidades, UI y Comandos Básicos</h4>

      <p>
      Dentro del CLI tenemos varias funcionalidades extras para facilitar el desarrollo del proyecto.
      <br>→ Detección de errores le linteo.
      </p>

      <div class="comand">
      <span>
      npm run lint
      </span>
      </div>

      <p class="text2">
      → Aplicación de producción.
      </p>

      
      <div class="comand">
      <span>
      npm run build
      </span>
      </div>

      <p class="text2">
      → Instala de manera global el comando serve.
      </p>

      <div class="comand">
      <span>
      npm i -g serve
      </span>
      </div>

      <p class="text2">
      → Levantar un localhost con la aplicación de producción.
      </p>

      <div class="comand">
      <span>
      serve -s dist
      </span>
      </div>

      <p class="text2">
      → Crea una aplicación web local, mediante la cual podemos gestionar los proyectos de Vue.
      </p>

      <div class="comand">
      <span>
      vue ui
      </span>
      </div>

      <iframe class="video" width="750" height="415" src="https://www.youtube.com/embed/znNfCne7d0Y" title="YouTube 
      video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media;
      gyroscope; picture-in-picture" allowfullscreen></iframe>

      </div>

      <div v-for="post in posts" :key="post.id">
        <div>
          <div>
            <router-link :to="{ name: 'PostDetail', params: { id: post.id } }">
              {{ post.title }}
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import auth from "../../common/auth";
import RepositoryFactory from "@/repositories/RepositoryFactory";
const PostsRepository = RepositoryFactory.get("posts");

export default {
  data: () => ({
    posts: []
  }),
  async created() {
    this.posts = await PostsRepository.getAll();
  },
  computed: {
    isAdmin() {
      return auth.isAdmin();
    }
  }
};
</script>

<style scoped>
.clear {
  clear: both;
}

h3{
  margin-top:20px;
  margin-bottom:10px;
  text-shadow: 0 0 0.2em #87F, 0 0 0.2em #87F,
	0 0 0.2em #87F;
}

h4{
  margin-top:20px;
  margin-bottom:20px;
  text-shadow: 0 0 0.2em rgb(255, 119, 232), 0 0 0.2em rgb(232, 119, 255),
	0 0 0.2em rgb(250, 119, 255);
}

.comand{
  position:absolute;
  background-color: #292929;
  border-width: 1px;
  border-style: solid;
  width:79.1%;
  height:2.2%;
  margin-left:100px;
  border-radius:10px;
  
}

span{
  color:#F3F3F3;
  float:left;
  padding-left: 15px;
  padding-top: 15px;
}

.text2{
  margin-top:100px;
}

.video1{
  margin-bottom:40px;
  box-shadow: 7px 10px 35px #000000;
  border-radius:10px;
  margin-top:30px;
}

.video{
  margin-top:130px;
  margin-bottom:30px;
  box-shadow: 7px 10px 35px #000000;
  border-radius:10px;
}

</style>
