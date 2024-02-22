<template>
<div>
    <h1>AZUL</h1>
    <Azul/>
    <h1>VERMELHO</h1>
    <Vermelho/>
</div>
</template>
<script>
import Azul from './azul.vue';
import Vermelho from './vermelho.vue';
export default {
    name: 'Cores',
    components: { Azul,
    Vermelho }
}
</script>