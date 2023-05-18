<template>
    <div>
        <button @click="primeiro(txt1,$event), segundo(txt2,$event), terceiro()">Ativar multiplos eventos</button>
        <p>{{ multi_eventos }}</p> <!--dados-->
    </div>
</template>

<script>
export default {
   name:'MultiplosEventos',
   data(){
    return{
        multi_eventos:'',
        txt1: 'Primeiro evento',
        txt2: 'Segundo evento'
    }
   },
   methods:{
    primeiro(txt1,e){
        this.multi_eventos = txt1
    },
    segundo(txt2,e){
        setTimeout(() => this.multi_eventos = txt2, 500);
    },
    terceiro(){
        setTimeout(() => this.multi_eventos = '', 1500); //vai limpar 
    }
   }

}
</script>

<style scoped>
    div{
        margin: 50px;
    }
</style>