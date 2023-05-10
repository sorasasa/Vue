<template>
  <div>
    <PrimeiroComponente/>
    <p>{{ teste }}</p>
  </div>
  
</template>
<!--aq usa o componente ao Importar e utilizar a tag dele -->
<script>
//componente em root da aplicação
import PrimeiroComponente from "./components/PrimeiroComponente.vue"

  export default{
    name: "app",
    components: {
      PrimeiroComponente
    },
    data(){
      return {
        teste: "testando"
      }
    }
  }
  

</script>