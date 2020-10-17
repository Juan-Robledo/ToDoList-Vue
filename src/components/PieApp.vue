<template>
    <footer>
        <p><slot></slot></p>
    </footer>
</template>

<script>
export default {
    name: 'PieApp'
}
</script>

<style scoped>
    footer{
        height: 50px;
        background-color: #662e99;
    }
    p{
        color: white;
        text-align: center;
        padding-top: 15px;
    }
</style>