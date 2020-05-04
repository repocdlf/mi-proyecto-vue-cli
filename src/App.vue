<template>
  <div>
    <div id="app">

    </div>
    <Navbar />
    <Binding/>
    <Estructura/>
    <Atributos/>
    <Contador/>
    <HelloWorld msg="Bienvenidos a Vue.js CLI" />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue"
import HelloWorld from "./components/HelloWorld.vue";
import Binding from "./components/Binding.vue";
import Estructura from "./components/Estructura.vue";
import Atributos from "./components/Atributos.vue";
import Contador from "./components/Contador/index.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Navbar,
    Binding,
    Estructura,
    Atributos,
    Contador
  }
};
</script>

<style>
#app {
}
</style>
