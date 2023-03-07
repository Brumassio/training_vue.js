<template>
  <div>
    <Header :esta_logado="true"/>
    <componente />
    <p class="pai">O dado do app é: {{ dado }}</p>
    <LifeCycle />
    <Pessoa />
  </div>

</template>

<script>
  import componente from './components/componente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'
  import Header from './components/Header.vue'

  export default {
    name: 'App',
    components: {
      componente,
      LifeCycle,
      Pessoa,
      Header
    },
    data() {
      return{
        dado: 'CORINTHIANS'
      }
    }
  }
</script>

<style>
  body{
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }
  .teste{
    background-color: blue;
  }
</style>