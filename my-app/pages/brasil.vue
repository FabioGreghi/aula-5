<template>
    <ul>
        <li> Nome Comum: {{ this.dados[0].name .common }} </li>
        <li> Nome Oficial: {{ this.dados[0].name .official }} </li>
        <li> Nome Moeda: {{ this.dados[0].currencies .BRL .name }} </li>
        <li> Simbolo Moeda: {{ this.dados[0].currencies .BRL .symbol }} </li>
        <li> Capital: {{ this.dados[0].capital }} </li>
        <li> Região: {{ this.dados[0].region }} </li>
        <li> Sub-Região: {{ this.dados[0].subregion }} </li>
        <li> Fronteiras: {{ this.dados[0].borders }} </li>
    </ul>
</template>

<script>
import brasil from "~/brasil.json"

export default {
    data(){
        return{
            dados:brasil,
        }
    }
}
</script>