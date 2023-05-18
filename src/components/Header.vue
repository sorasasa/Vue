<template>
<ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contato</a></li>
    <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>
</ul>
</template>
<script>
export default{
    name: 'Header',
    props: ['esta_logado']
}
</script>
 <!--o estilo escrito em scoped só se aplica numa area-->
<style scoped>
    ul{
        list-style: none; /*sumir com as bolinhas*/
        display: flex; /*item vai pro lado do outro*/
        background-color: #111;
        padding:20px;
    }
    li {
        margin-right: 10px; /**itens vao ter um espaçamento entre eles */
    }
    a {
        color: #ddd;
        text-decoration: none; /**tira o sublinhado */
        transition: .5s; /**a demora pra aparecer a cor */
    }
    a:hover {
        color: turquoise;
    }
/**estilização do cabeçario */
</style>
