<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld 
        msg="Práctica sencilla" 
        contenido="Practicando con propiedades reactivas"
        contenido2="contenido del atributo <<<<<<<"
      />
    </div>
  </header>

  <main>
    <PropiedaesReactivas1Vue></PropiedaesReactivas1Vue>
    <PropiedadesReactivasObjetos
      titulo="Tipos complejos (Objetos)"
    ></PropiedadesReactivasObjetos>
  </main>
</template>

<script setup>
  import HelloWorld from './components/HelloWorld.vue'
  import PropiedaesReactivas1Vue from './components/practicas/PropiedaesReactivas1.vue';
  import PropiedadesReactivasObjetos from './components/practicas/PropiedadesReactivasObjetos.vue';


</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
