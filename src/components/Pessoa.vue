<template> <!--2--><!--pensa como se fosse as classes do poo-->
<div>
    <h3>Essa é a descrição da pessoa:{{ nome }}</h3><!--sempre precisa exportar pro App-->
    <Info :email="email" :esta_trabalhando=true /><!--prop--><!--o email q ta em data vai ser enviado via props pro componente info-->
    <Form/><!--importou componente--> 
</div>
</template>

<script>
import Info from "./Info.vue"
import Form from "./Form.vue"
export default {
    name: 'Pessoa',
    components: { //precisa colocar porq ESSE component vai depender de outros componentes
        Info,
        Form
    },
    data(){
        return{
            nome: 'Matheus',
            email: 'abc@email.com'
        }
    }
}
</script> 