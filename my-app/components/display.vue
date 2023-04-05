<template>
    <section class="display">{{ valor }}</section>
</template>

<script>
export default{
    props: {
        valor:{
            required: true 
        }
    }
}
</script>

<style scoped>
    .display {
        width: 100%;
        height: 50px;
        border: 1px solid gray;
        background-color: white;
    }
</style>