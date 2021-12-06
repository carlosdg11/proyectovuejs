<template>
  <div class="text-center">
    <div>
      <h2>¿Qué es Vue.js?</h2>
      <p>
      <strong>Vue.js</strong> (también llamado Vue o VueJS) es un <strong>framework progresivo</strong> Javascript para 
      crear interfaces de usuario, o en otras palabras, se trata de una «capa» añadida 
      a Javascript formada por herramientas, convenciones de trabajo y un lenguaje particular
      que nos permite crear aplicaciones de forma rápida, agradable, sencilla y muy práctica.
      </p>

     <img id="imgvue" src="../assets/vue.png">

      <p>
      Vue es un framework frontend, es decir, que si vienes de framework del estilo de Laravel 
      <strong>(PHP)<strong>, Ruby on rails <strong>(Ruby)</strong>, Spring </strong>(Java) </strong>u otros framework de backend, te encontrarás 
      múltiples diferencias. En los últimos años se ha popularizado la creación de aplicaciones
      de tipo SPA (Single Page Application), que es la categoría donde se encuentra <strong>Vue</strong>
      , <strong>React</strong>, <strong>Angular</strong>, etc...
      </p>

      <p>
      Fue creado por <a href="https://evanyou.me/"><strong>Evan You</strong></a> ex trabajador de Google, 
      quien, es importante mencionar, fue desarrollador Angular. Vue fue lanzado en el año 2014. 
      Aunque inicialmente fue pensado para ser un biblioteca personal, la comunidad hizo que el proyecto 
      creciera a un ritmo impresionante, posicionándolo hoy en día como uno de los Frameworks web más populares,
      junto con <strong>Angular</strong> y <strong>React</strong>.
      </p>

      <a href="https://www.indiehackers.com/podcast/078-evan-you-of-vue">
      <img id="imgevan" src="../assets/evanyou.png"></a>


    </div>
  </div>
</template>

<style>

h2{
  margin-top:20px;
  margin-bottom:20px;
  font-size: 50px;
  color: red;
}

p{
  text-align: justify;  
  font-size: 20px;
  margin-top: 40px;
  padding-left:100px;
  padding-right: 100px;
  font-family: Tahoma;
}

#imgvue{
  width: 55%;
  max-width:100%;
  margin-bottom:-45px;
}

#imgvue:hover{
    -webkit-transform:scale(1.1);
    transform:scale(1.1);
}

#imgevan{
  width: 50%;
  max-width:100%;
  border-radius:10px;
  margin-bottom:45px;
}

#imgevan:hover{
    -webkit-transform:scale(1.1);
    transform:scale(1.1);
}

</style>

