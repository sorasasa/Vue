<template>
    <h1>Meu nome é: {{ nome }} </h1>
</template>

<script>
export default{
name: "LifeCycle",
data(){
    return{
        nome: 'ainda nao sei',
    }
    },
created(){ //acessa e altera as propriedades de DATA (do app)
    setTimeout(() => {
        this.nome = "matheus" 
    }, 1000);
    this.LifeCycle();
    },
mounted(){ //esse acima de created na hierarquia
    setTimeout(() => {
        this.nome = "pedro" 
    }, 2000);//eventos acontecendo em determinada etapa da aplicação
    this.LifeCycle();
    },
methods:{
    LifeCycle(){
        console.log("Executou!")
    }
    }
}
</script>