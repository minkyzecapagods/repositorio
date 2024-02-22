<template>
  <div>
  <header>
      <img alt="Vue logo" src="@/components/imagens/logo.png" width="100px">
      <h1>Aula 3 - Vue.js</h1>
    </header>
    <div id="caixa">
      <h1 id="pratica">Prática 1:</h1>
      <p id="descricao">Adicionar um componente e escrever uma variável.</p>
      <BoasVindas/>
    </div>
    <div id="caixa">
      <h1 id="pratica">Prática 2:</h1>
      <p id="descricao">
        Criar e chamar funções, usar operadores lógicos e matemáticos, concatenar strings e programar botões.
      </p>
      <CaixaLikes/>
    </div>
    <div id="caixa">
      <h1 id="pratica">Prática 3:</h1>
      <p id="descricao">
        Aplicar diretivas e usar variáveis como atributos.
      </p>
      <CaixaMagica/>
    </div>
    <div id="caixa">
      <h1 id="pratica">Prática 4:</h1>
      <p id="descricao">
        Aplicar diretivas e usar variáveis como atributos.
      </p>
      <PerguntaSimples/>
    </div>
    <div id="caixa">
      <h1 id="pratica">Prática 3, 4 e 5 - Dia 4:</h1>
      <NuxtLink to="cores/azul">Azul</NuxtLink>
      <NuxtLink to="cores/vermelho">Vermelho</NuxtLink>
      <NuxtLink to="cores/cores">Index</NuxtLink>
      <NuxtLink to="cores/_arq">Arquivos</NuxtLink>
      <NuxtLink to="indexmuco">Músicas e cores</NuxtLink>
    </div>
  </div>
</template>

<script>
import BoasVindas from '../components/BoasVindas.vue';
import CaixaLikes from '../components/CaixaLikes.vue'
import CaixaMagica from '../components/CaixaMagica.vue';
import NuxtLogo from '../components/NuxtLogo.vue';
import PerguntaSimples from '../components/PerguntaSimples.vue'

export default {
    name: 'IndexPage',
    components: { BoasVindas,
    CaixaLikes,
    CaixaMagica,
    PerguntaSimples, NuxtLogo }
}
</script>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #d6f1e5;
  padding: 30px;
  padding-left: 150px;
  padding-right: 150px;
}

#caixa {
  background-color: #f3f5f7; ;
  padding: 30px;
  padding-top: 0px;
  min-height: 200px;
  min-width: max-content;
  display: flex;
  border-left: 5px solid #4abf8a;
  border-bottom: 5px solid #4abf8a;
  border-top: 1px solid lightgray;
  box-shadow: -5px 5px #233056;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 50px;
}
</style>
