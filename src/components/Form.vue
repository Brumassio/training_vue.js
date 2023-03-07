<template>
    <div>
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model="name">
                <!-- <InputText/> -->
            </div>
            <div>
                <input type="text" v-model="email">
                <!-- <InputText/> -->
            </div>
            <div>
                <Submit/>
            </div>
        </form>
        <p>Chesque</p>
    </div>

</template>

<script>
    import InputText from './form/InputText.vue';
    import Submit from './form/Submit.vue';
    export default{
        name: 'Form',
        components: {
            Submit,
            InputText
        },
        data(){
            return{
                name: '',
                email: ''
            }
        },
        methods: {
            enviarFormulario(e){
                e.preventDefault()
                const name = this.name;
                const email = this.email;
                console.log("Formulário enviado");
                console.log("O nome é:"+ name);
                console.log("O email é:"+ email);
            }
        }
    }
</script>

<style scoped>
    p {
        margin: 50px
    }
</style>