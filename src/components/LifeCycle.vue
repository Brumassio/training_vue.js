<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
import { onMounted } from 'vue';

export default {
    name: 'LyfeCycle',
    data(){
        return{
            nome: 'Seila bro'
        }
    },

    created(){
        setTimeout(() => {
            this.nome = 'Diogo' 
        }, 1000);  
        this.lifeCycle()
    },
    mounted(){
        setTimeout(() => {
            this.nome = 'Daniel' 
        }, 2000); 
        this.lifeCycle()
    },
    methods:{
        lifeCycle(){
            console.log("Executou");
        }
    }

}
</script>