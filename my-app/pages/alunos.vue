<template>
    <form @submit.prevent="$e => salvaraluno()">
        <input type="text" placeholder="nome" v-model="nome">
        <input type="number" placeholder="idade" v-model="idade">
        <input type="text" placeholder="serie" v-model="serie">
        <button>salvar</button>
    </form>
    <hr>
    <ul v-for="(aluno,index) in this.dados"> 
        <li> codigo: {{ index }} </li>
        <li> nome: {{ aluno.nome }} </li>
        <li> idade {{ aluno.idade }} </li>
        <li> série {{ aluno.serie }} </li>
        <button @click="deletar(index)"> deletar </button>
    </ul>
</template>

<script>
import aluno from "~/alunos.json"

export default {
    data() {
        return{
            dados: aluno,
            nome: "",
            idade: "",
            serie: ""
        }
    },
    methods: {
        salvaraluno() {
            this.dados.push({"nome": this.nome, "idade": this.idade, "serie": this.serie})
        },
        deletar(index) {
            this.dados.splice(index, 1)
        },
    }
}
</script>