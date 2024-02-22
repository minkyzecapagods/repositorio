<template>
<div id="pergunta">
    <h2>Qual é o nome do prédio que estamos agora?</h2>
    <input id="caixa-input" type="text" v-model="resposta" placeholder="Responda aqui...">
    <button id="botao-curtidas" v-on:click="checar()">Responder</button>
    <h3 v-if="correto">Correto</h3>
    <h3 v-if="incorreto">Incorreto</h3>
</div>
</template>

<script>
export default {
    data(){
        return {
            resposta: "",
            correto: false,
            incorreto: false,
            cor: ""
        }
    },
    methods:{
        checar(){
            if (this.resposta == this.$parent.predio) {
                this.correto = true;
                this.incorreto = false;
            }
            else {
                this.incorreto = true;
                this.correto = false;
            }
        }
    }
}
</script>

<style>
#pergunta {
    background-color: #0c4a6e;
    color: white;
    padding: 30px;
    padding-top: 10px;
    border-radius: 15px;
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 230px;
}

#caixa-input {
    font-size: large;
    padding: 7px;
}
</style>