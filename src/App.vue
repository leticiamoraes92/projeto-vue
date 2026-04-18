<template>
  <div class="container">
    <h1>Gerador de Frases </h1>

    <p class="frase">{{ frase }}</p>

    <button @click="gerarFrase">Gerar Frase</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      frases: [
  "Código limpo é melhor que código complicado.",
  "Primeiro faça funcionar, depois faça bonito.",
  "Erros são provas de que você está tentando.",
  "Programar é transformar café em código.",
  "Todo bug é uma oportunidade de aprender.",
  "A prática leva à perfeição no código.",
  "Nunca confie no código que você não escreveu.",
  "Se está funcionando, não mexa... ou mexa com cuidado 😄",
  "Um bom programador resolve problemas, não cria mais.",
  "Código simples é mais fácil de manter.",
  "Debugar é como ser detetive em um crime que você mesmo cometeu.",
  "Aprender a programar é aprender a pensar.",
  "Pequenos passos constroem grandes sistemas.",
  "A melhor forma de aprender é praticando.",
  "Código bem feito economiza tempo no futuro."
],
      frase: "Clique no botão para gerar uma frase"
    }
  },
  methods: {
    gerarFrase() {
      const index = Math.floor(Math.random() * this.frases.length)
      this.frase = this.frases[index]
    }
  }
}
</script>

<style>
.container {
  text-align: center;
  margin-top: 100px;
  font-family: Arial, sans-serif;
}

.frase {
  font-size: 20px;
  margin: 20px 0;
  color: #333;
}

button {
  padding: 12px 20px;
  font-size: 16px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>