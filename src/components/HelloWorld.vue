<template>
  <div class="greetings">
    <label>Insira sua pergunta</label>
    <input type="text" v-model="question"/>
    <p>{{ respostaFinal }}</p>
    <button @click="gerarResposta">Perguntar</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
      return{
        question: "",
        respostaFinal: "",
        answer: [
          'Com certeza',
          'É... não tenho certeza!',
          'Claro que não',
          'Acho difícil',
          'Possívelmente não']
      }
    },
    methods: {
      gerarResposta() {
          const respostaIndex = Math.floor(Math.random() * 5);
          this.respostaFinal = this.answer[respostaIndex];
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
