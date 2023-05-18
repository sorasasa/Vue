<template>
    <div>
        <button @click="$emit('mudarImg')">Trocar foto de perfil</button>
<!--quando clicar vai chamar o emitir metodo, e dentro do metodo tem a imagem-->
    </div>
</template>
<script>
export default {
    name: 'MudarImg',
    emits: ['mudarImg']
}
</script>