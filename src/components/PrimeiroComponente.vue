<template>
    <div>
        <h2>Olá Vue!</h2>
        <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
        <MultiplosEventos/>
        <Reutilizacao/>
    </div>
</template>
 <!--é criado um componente e exportado-->
<script>
    import MultiplosEventos from "./MultiplosEventos.vue"
    import Reutilizacao from "./Reutilizacao.vue"

    export default{
        nome: "PrimeiroComponente",
        components:{
            MultiplosEventos,
            Reutilizacao
        },
        data(){ ///retorno de dados
            return { //coloca dados no objeto pra ser usado no componente
                nome: "Matehus", //dado chamado nome
                profissao: "programador"
            }
        }
    }
</script>