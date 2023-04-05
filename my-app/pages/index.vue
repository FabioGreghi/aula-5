<template>
    <main>
        <display 
            :valor="display"
        />
        <numeros 
            @digitar="digitar"
        />
        <acoes 
            @limpar="limpar"
            @somar="somar"
            @subtrair="subtrair"
            @igual="igual"
        />
    </main>
</template>

<script>
    export default {
        data(){
            return{
                display: "",
                n1:"",
                n2:"",
                op:""
            }
        },
        methods:{
            subtrair(){
                this.n1 = parseInt(this.display), 
                this.display = ""
                this.con = "subtrair"
            },
            somar(){
                this.n1 = parseInt(this.display), 
                this.display = ""
                this.con = "somar"
            },
            igual(){
                if (this.con === "somar"){
                    this.n2 = parseInt(this.display),
                    this.display = this.n1 + this.n2
                }else{
                    this.n2 = parseInt(this.display),
                    this.display = this.n1 - this.n2
                }
            },
            limpar(){
                this.display = ""
            },
            digitar(valor){
                this.display = this.display + valor;
            }
        }
    }
</script>

<style scoped>
    main{
        display: block;
        margin: auto;
        margin-top: 200px;
        padding: 20px;
        width: 500px;
        height: 500px;
        background-color: aqua;
    }
</style>