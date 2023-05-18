<template><!--3-->
<div>
    <br/>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias para back-end: </p>
 <!--vai imprimir os textos de cada um dos elementos do array-->
    <ul><!--se coloca aq vai causar repetição-->
        <li v-for="(tech, index) in backend_tech" v-bind:key="index">{{ tech }}
        </li><!--indice de cada elemento-->
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
        <li v-for="tech in frontend_tech" :key="tech.id">{{ tech.language }}</li><!--explicação embaixo-->
    </ul>
    <div>
    <button @click="showEmail">{{ textoBotao }}</button>
    </div><!--vai mostrar via props, nao via data()-->
    <p v-show="mostrar_email">Mande um email para {{ email }}</p>
    <p class="teste">Para acessar meu portifolio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
    <Picture/>
</div>
</template>

<script>
import Picture from "./Picture.vue"

export default {
    name: 'Info',
    components: { //picture vai depender de componente(como se fosse getter e setter)
        Picture //precisa reafirmar que o arquivo ta aqui
    },
    props:{//precisa ficar no mesmo arquivo onde chama
        email: String, 
        esta_trabalhando: Boolean
    },
    data(){
        return {
            mostrar_email: false,
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar e-mail',
            backend_tech: ['JavaScript', 'PHP', 'Python'],
            frontend_tech: [
                {id: 1, language:'HTML'},
                {id: 2, language:'CSS'},
                {id: 3, language:'Vue'}
            ]
        }
    },
    methods:{
        showEmail(){
          this.mostrar_email = !this.mostrar_email //clica uma vez vira true, clica dnv vira false
          if(!this.mostrar_email){ //mostrar email for falso
            this.textoBotao = 'Mostrar e-mail'
          }else{
            this.textoBotao = 'Esconder e-mail'
          }
        }
    }
}
</script>
<style> 
 .paragrafo-pai{
    color: purple;
 }
</style>
 <!--o index serve para pegar o indice exato de cada item da lista no momento em que o loop inicia, exemplo se tem 7 items na lista, cada item tera um id de 0 a 6 faendo assim um id unico que numca ira se repetir dentro do loop, compreendeu?-->