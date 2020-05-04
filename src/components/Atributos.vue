<template>
  <section class="src-components-atributos">
    <div class="jumbotron mt-3">
      <h2>Componente Atributos</h2>
      <hr />
      <!-- -------------------------------------- -->
      <!-- -------------------------------------- -->
      <h4><u>:style</u></h4>
      <br>
      <button class="btn btn-success my-3" @click="estado1=!estado1">Cambiar</button>
      <p :style="{color: 'white',backgroundColor: estado1? 'green':'red', borderRadius:'10px', padding: '10px'}">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Provident impedit soluta ea et labore temporibus quae, quis dolore sed quasi corporis dolores molestiae ratione voluptatem accusantium quaerat. Neque, nam repudiandae.
      </p>

      <hr>
      <!-- -------------------------------------- -->
      <!-- -------------------------------------- -->
      <h4><u>:class</u></h4>
      <br>
      <button class="btn btn-success my-3" @click="estado2=!estado2">Cambiar</button>
      <p :class="['text-white',{'bg-success': estado2,'bg-danger': !estado2}]">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Provident impedit soluta ea et labore temporibus quae, quis dolore sed quasi corporis dolores molestiae ratione voluptatem accusantium quaerat. Neque, nam repudiandae.
      </p>


      <hr>

    </div>
  </section>
</template>

<script lang="js">

  export default  {
    name: 'src-components-atributos',
    props: [],
    mounted () {

    },
    data () {
      return {
        estado1: true,
        estado2: true
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="css">
.src-components-atributos {
}
.jumbotron {
  background-color: cornflowerblue;
  color: rgb(0, 0, 116);
}

hr {
  background-color: #333;
}
</style>
