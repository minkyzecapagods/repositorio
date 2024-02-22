<template>
    <div id="esconda">
        <button id="botao-curtidas" v-on:click="trocar()">Caixa Mágica</button>
        <img id="sonic" alt="Imagem Secreta" v-if="aparece" :src="require(`./imagens/${source}`)" width="250px">
        
    </div>
</template>

<script>
export default {
    data(){
        return {
            counter: 0,
            aparece: false,
            source: 'sonic.png'
        }
    },
    methods:{
        trocar(){
            this.counter++;
            this.aparece = !this.aparece
            if (this.counter > 9) {
                this.source = 'alfa.png'
            }
        }
    }
}
</script>

<style>
#esconda {
    background-color: #0c4a6e;
    color: white;
    padding: 30px;
    padding-top: 10px;
    border-radius: 15px;
    margin-top: 10px;
    display: flex;
    align-items: center;
    min-width: 450px;
    min-height: 400px;
    flex-direction: row;
}

#sonic {
    padding-left: 40px;
}
</style>