<template>
    <div class="">
        <h1>Olá Vue !</h1>
        <p>Meu nome é {{ nome }} e sou {{ profissao }}</p>
        <MultiplosEventos /> 
        <Reutilizacao/>       
    </div>

</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue'
    import Reutilizacao from './Reutilizacao.vue';
    export default{
        name: 'componente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return {
                nome: "Cássio",
                profissao: "Goleiro"
            }
        }
    }

</script>
