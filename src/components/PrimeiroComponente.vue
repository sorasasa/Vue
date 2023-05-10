<template>
    <div>
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
    </div>
</template>
 <!--é criado um componente e exportado-->
<script>
    export default{
        nome: "PrimeiroComponente",
        data(){ //retorno de dados
            return { //coloca dados no objeto pra ser usado no componente
                nome: "Matehus", //dado chamado nome
                profissao: "programador"
            }
        }
    }
</script>