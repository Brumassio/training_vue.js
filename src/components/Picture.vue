<template>
    <div>
        <img v-if="verifica" :src="avatar" :alt="descricao">
        <img v-else :src="avatar2" :alt="descricao">
        <MudarImagem @mudar-imagem="trocarImagem"/>
    </div>

</template>

<script>
import MudarImagem from './MudarImagem.vue'
    export default{
  components: { MudarImagem },
        name: 'Picture',
        data(){
            return{
                avatar: "/img/invencivel.png",
                avatar2: "/img/foto_boa3.jpg",
                descricao: "Xesque",
                verifica: true
            }
        },
        methods: {
            trocarImagem(){
                this.avatar = "/img/dianho3.png"
            }
        }
    }
</script>