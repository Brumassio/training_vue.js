<template>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
        <li v-if="esta_logado"> <a href="#">Meu Perfil</a></li>
    </ul>
</template>

<script>
    export default{
        name: 'Header',
        props: ["esta_logado"]
    }
</script>

<!-- scoped fala q é só desse componente -->
<style scoped>
    ul{
        list-style: none;
        display: flex;
    }
    li{
        margin-right: 10px;
    }
    a{
        color: #ddd;
        text-decoration: none;
        transition: .5s;
    }
/* deixa turquesa quando coloca o mouse em cima  */
    a:hover {
        color: turquoise;
    }
</style>