<template>
    <div id="curta">
        <h1 id="titulo-curtidas">Esse curso {{ espaco }} curtidas</h1>
        <button id="botao-curtidas" v-on:click="curtir()">Curtir</button>
    </div>
</template>

<script>
export default {
    data(){
        return {
            likes: 0,
            espaco: 'não tem'
        }
    },
    methods:{
        curtir(){
            this.likes++;
            if (this.likes != 0) {
                this.espaco = 'tem ' + this.likes
            }
        }
    }
}
</script>

<style>
#titulo-curtidas {
margin: 10px;
margin-bottom: 30px;
}

#botao-curtidas {
    background-color: #4abf8a;
    color: white;
    padding: 25px;
    padding-top: 10px;
    padding-bottom: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: medium;
    font-weight: bold;
    transition: all 0.15s;
    margin-top: 20px;
}

#botao-curtidas:hover {
    background-color: #4abf8a93;
}

#botao-curtidas:active {
    background-color: #4abf8a41;
}

#curta {
    background-color: #0c4a6e;
    color: white;
    padding: 30px;
    padding-top: 10px;
    border-radius: 15px;
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>