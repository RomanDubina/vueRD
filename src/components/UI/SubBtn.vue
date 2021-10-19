<template>

        <button><slot></slot></button>

</template>

<script>
    export default {

    }
</script>

<style scoped>
    button{
        border: none;
        background: bisque;
        padding: 12px 50px;
        cursor: pointer;
        font-size: 21px;
        text-transform: uppercase;

    }
</style>