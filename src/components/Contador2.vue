<template>

  <section class="src-components-contador-2">
  <div class="jumbotron mt-3" :style="{'background-color': colorDeFondo}">
    <h2>Componente {{titulo}}</h2>
    <hr />
    <button :class="['btn', getEstilos(),'my-2']" @click="contar()">Contar {{mostrarContador}}</button>
  </div>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-contador-2',
    /*props: {
      valorInicial: String,
      estilo: String,
      colorDeFondo: String,
      titulo: String
    },*/
    props: [
      'valorInicial',
      'estilo',
      'colorDeFondo',
      'titulo'
    ],

    // https://vuejs.org/v2/guide/instance.html#Lifecycle-Diagram

    //-----------------------------------------------------
    // CICLO DE VIDA DE LOS COMPONENTES DE VUE
    //-----------------------------------------------------

    // Instanciacion del componente en la vista
    beforeCreate () {
      console.log('Contador 2 -> beforeCreate')
    },
    created () {
      console.log('Contador 2 -> created')
    },

    // Montaje del componente en la vista
    beforeMount () {
      console.log('Contador 2 -> beforeMount')
    },
    mounted () {
      console.log('Contador 2 -> mounted');
      /** Activo proceso de timer */
      this.refInterval = setInterval(() => {
        this.timer++
        console.log('Contador 2 -> TIMER',this.timer);
      }, 2000);
    },

    // Actualizacionde la vista del componente
    beforeUpdate () {
      console.log('Contador 2 -> beforeUpdate')
    },
    updated () {
      console.log('Contador 2 -> updated')
    },

    // Destruccion del componente
    beforeDestroy () {
      console.log('Contador 2 -> beforeDestroy')
    },
    destroyed () {
      console.log('Contador 2 -> destroyed')
      /** Desactivo proceso de timer */
      clearInterval(this.refInterval)
    },

    data () {
      return {
        contador: this.valorInicial,
        timer: 0,
        refInterval: ''
      }
    },
    methods: {
      contar() {
        this.contador++
        //console.log(`El ini del contador es btn-${this.estilo}`)
      },
      getEstilos() {
          return 'btn-' + this.estilo
      }
    },
    computed: {
      mostrarContador(){
        return this.contador;
      }
    }
}


</script>

<style scoped lang="css">
  .src-components-contador-2 {

  }
  .jumbotron {
  background-color: rgb(180, 60, 80);
  color: white;
  }

  hr {
    background-color: #444;
  }
</style>
