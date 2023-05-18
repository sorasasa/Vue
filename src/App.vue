<template> <!--1 na hierarquia-->
  <div>
    <Header :esta_logado="true"/>
    <PrimeiroComponente/>
    <p class="paragrafo-pai">{{ teste }}</p>
    <LifeCycle/>
    <Pessoa/>
  </div>
  
</template>
<!--aq usa o componente ao Importar e utilizar a tag dele -->
<script>
//componente em root da aplicação
import Header from "./components/Header.vue"
import PrimeiroComponente from "./components/PrimeiroComponente.vue"
import LifeCycle from "./components/LifeCycle.vue"
import Pessoa from "./components/Pessoa.vue"

  export default{
    name: "app",
    components: {
      Header, //tem q declarar o nome dos componentes assim como é feito no componente deles
      PrimeiroComponente,
      LifeCycle,
      Pessoa 
    }, 
    data(){
      return {
        teste: "testando"
      }
    }
  }
</script>  <!--estilo global funciona em qualquer uma das hierarquias-->
<style>
  body { 
    background-color: powderblue;
    color:#000;
    font-family: Arial, Helvetica, sans-serif;
  }
  a {
    color:red;
  }
  .teste {
    background-color: black;
    color:lavender;
    padding:10px;
  }
</style>