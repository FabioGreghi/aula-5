<template>
        <section class="botoes">
            <button @click="($e) => $emit('digitar', 0)">0</button>
            <button @click="($e) => $emit('digitar', 1)">1</button>
            <button @click="($e) => $emit('digitar', 2)">2</button>
            <button @click="($e) => $emit('digitar', 3)">3</button>
            <button @click="($e) => $emit('digitar', 4)">4</button>
            <button @click="($e) => $emit('digitar', 5)">5</button>
            <button @click="($e) => $emit('digitar', 6)">6</button>
            <button @click="($e) => $emit('digitar', 7)">7</button>
            <button @click="($e) => $emit('digitar', 8)">8</button>
            <button @click="($e) => $emit('digitar', 9)">9</button>
        </section>
</template>

<style scoped>
    .botoes button{
        width: 50px;
        height: 50px;
    }
</style>