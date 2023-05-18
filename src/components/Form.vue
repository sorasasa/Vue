<template>
<form action="" @submit="enviarFormulario($event)"><!--metodo ativado quando enviar-->
 <div>
    <h2>Meu Formulário: </h2>
    <input type="text" v-model="name">
 </div>
 <div>
   <input type="text" v-model="email">
 </div>
 <div>
    <Submit/><!--mesmo usando o mesmo componente dnv, eles são diferentes-->
    <p>{}</p>
    <p>{}</p>
    <p>{}</p>
 </div>
</form>
</template>
<script>
import InputText from "./form/InputText.vue"
import Submit from "./form/Submit.vue"

export default {
    name: 'Form',
    components:{ //depende das caracteristicas das outras classes ex
        InputText,
        Submit 
    },
    data(){
      return{
         name:'',
         email:''
      }
    },
    methods:{
//$event é vazia e aqui é oq ela representa
      enviarFormulario(e){ 
         e.preventDefault(); //evita dar reload na pagina
//vai substituir os dados do DATA, ao preencher o v-model no formulario
         const name = this.name; 
         const email = this.email;

         console.log("formulario enviado");
         console.log("o nome é: " + name);
         console.log("o email é: " + email)

         //ajax
         //inserir no banco de dados
      }
    }
}
</script>
<style scoped>
p {
   margin: 50px;
}
</style>
