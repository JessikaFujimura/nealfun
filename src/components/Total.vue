<template>
    <p class="total">
        ${{ total }}
    </p>
</template>

<script>
export default {
    name: "Total",
    props: ['total'],
}
</script>

<style scoped>
.total {
    color: white;
    background: rgba(0, 0, 0, 0) linear-gradient(rgb(46, 204, 113), rgb(26, 188, 156)) repeat scroll 0% 0%;
    padding: 20px;
    margin: 10px 0px;
    font-size: 32px;
    font-weight: bold;
    text-align: center;
    top: 0px;
    position: sticky;
    z-index: 9999;
}
</style>