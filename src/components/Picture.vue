<template>
    <div>
        <img :src="avatar" :alt="descricao"> <!--o ':'serve como v-bind:-->
        <!--emit ativou o metodo trocarImg-->
        <MudarImg @mudar-img="trocarImg"/> <!--metodo no componente-->
    </div>
</template>
<script>
import MudarImg from "./MudarImg.vue"
export default { /**é o nome do arquivo SEMPRE tem q colocar */
    name: 'Picture',
    components: {
        MudarImg
    },
    data(){
        return{
            avatar: '/img/avatar.png',
            descricao: 'Matheus Battisti'
        }
    },
    methods: {
       trocarImg(){
        this.avatar = '/img/avatar2.png'
//quando @click no botao vai chamar o evento 
       } 
    }
}
</script>