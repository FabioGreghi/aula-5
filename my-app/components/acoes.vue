<template>
    <section class="acoes">
        <button @click="($e) => $emit('somar')">+</button>
        <button @click="($e) => $emit('subtrair')">-</button>
        <button @click="($e) => $emit('igual')">=</button>
        <button @click="($e) => $emit('limpar')">C</button>
    </section>
</template>

<style scoped>
    .acoes button{
        width: 50px;
        height: 50px;
    }
</style>